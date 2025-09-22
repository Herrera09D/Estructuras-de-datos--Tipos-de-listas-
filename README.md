# Implementación y Análisis de Listas Enlazadas en Python

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/[TU_USUARIO_DE_GITHUB]/[NOMBRE_DEL_REPOSITORIO]/blob/main/[NOMBRE_DEL_NOTEBOOK].ipynb)

**[IMPORTANTE: Edita el enlace de arriba! Reemplaza `[TU_USUARIO_DE_GITHUB]`, `[NOMBRE_DEL_REPOSITORIO]` y `[NOMBRE_DEL_NOTEBOOK].ipynb` con tus datos reales para que el botón funcione.]**

---

## Descripción del Proyecto

Este repositorio contiene la implementación y el análisis de rendimiento de tres estructuras de datos fundamentales: **Lista Simplemente Enlazada (LSE)**, **Lista Doblemente Enlazada (LDE)** y **Lista Doblemente Enlazada Circular (LDEC)**. Todas las implementaciones se realizaron en Python utilizando un nodo cabecera (sentinela) para simplificar las operaciones en los casos borde.

El objetivo principal de este trabajo es contrastar la complejidad teórica de las operaciones fundamentales (`insertar`, `eliminar` y `buscar`) con mediciones empíricas de sus tiempos de ejecución, analizando cómo escalan a medida que aumenta el número de elementos.

### Contexto Académico
*   **Asignatura:** Estructura de Datos y Análisis de Algoritmos
*   **Profesor:** Omar Portilla
*   **Semestre:** 2025-2

### Integrantes del Equipo
*   [Nombre Completo del Estudiante 1]
*   [Nombre Completo del Estudiante 2]
*   [Nombre Completo del Estudiante 3]
*   [Nombre Completo del Estudiante 4]

---

## Estructuras Implementadas

Se desarrollaron y probaron las siguientes clases de listas enlazadas:

1.  **`SinglyLinkedList` (LSE):** Lista con nodos que tienen un único enlace al siguiente elemento.
2.  **`DoublyLinkedList` (LDE):** Lista con nodos que tienen enlaces tanto al elemento siguiente como al anterior.
3.  **`CircularDoublyLinkedList` (LDEC):** Lista doblemente enlazada donde el último elemento apunta al primero (sentinela) y viceversa, formando un ciclo.

---

## Metodología de Análisis

El análisis de algoritmos se abordó desde dos perspectivas complementarias:

### 1. Modelo Teórico
Se derivó la complejidad asintótica (notación Big O/Theta) para las operaciones `insertar`, `eliminar` y `buscar` en cada una de las estructuras, considerando el mejor y el peor caso.

### 2. Modelo Empírico
Se cronometraron los tiempos de ejecución de las operaciones utilizando `time.perf_counter()` para obtener mediciones precisas. Los experimentos se realizaron para diferentes tamaños de entrada (`n`) y se graficaron los resultados para visualizar las tendencias de rendimiento.

*   **Herramientas:** Python, Google Colab, Pandas (para la gestión de datos), Matplotlib y Seaborn (para la visualización).

---

## ¿Cómo Ejecutar el Proyecto?

La forma más sencilla de ejecutar y verificar los resultados es a través de Google Colab:

1.  **Hacer clic en el botón "Open in Colab"** que se encuentra al inicio de este README.
2.  Una vez abierto el notebook, ejecutar todas las celdas en orden desde el menú `Entorno de ejecución` > `Ejecutar todas`.
3.  El notebook generará las tablas de resultados y las gráficas comparativas de rendimiento al final del documento.

---

## Resultados y Conclusiones

Los resultados empíricos obtenidos confirman de manera consistente la complejidad teórica analizada:

*   Las operaciones de **tiempo constante (Θ(1))**, como `insert_head` y la búsqueda/eliminación en el mejor de los casos, muestran un tiempo de ejecución plano que no se ve afectado por el tamaño de la lista.
*   Las operaciones de **tiempo lineal (Θ(n))**, como la búsqueda y eliminación en el peor de los casos, muestran un tiempo de ejecución que crece de forma lineal y proporcional al número de elementos `n`.
*   Se destaca la eficiencia de la **LDEC** para realizar la operación `insert_tail` en tiempo constante (Θ(1)), una ventaja significativa sobre las otras dos estructuras donde esta operación sería de orden lineal.
