# Análisis Comparativo: Factorial Recursivo e Iterativo en Python y C
Introducción
Este proyecto tiene como objetivo analizar y comparar la eficiencia de dos enfoques para calcular el factorial de un número entero positivo 𝑛

- Método Recursivo: la función se llama a sí misma hasta alcanzar el caso base.

- Método Iterativo: se utiliza un bucle para acumular el resultado paso a paso.

La comparación se realiza en dos lenguajes de programación: Python y C, midiendo el tiempo de ejecución y el consumo de memoria.
Finalmente, se generan gráficas y tablas que muestran el rendimiento de cada enfoque.

## Descripción de las Implementaciones
### Python
En Python, las funciones se implementaron así:
- facto_i(n) → cálculo iterativo del factorial mediante un bucle for.
- facto_r(n) → cálculo recursivo con caso base en 𝑛 = 0 n = 0 o 𝑛 = 1.

Para medir eficiencia:
- Tiempo → time.time() para medir segundos transcurridos.
- Memoria → memory_usage() de memory_profiler para registrar el uso máximo.
- Visualización → matplotlib para generar gráficas comparativas de tiempo y memoria.

Archivo principal de ejecución:
medir_tiempo_memoria.py

Este archivo recorre una lista de valores de 𝑛, ejecuta ambas funciones, guarda resultados y genera las gráficas:
- grafica_tiempo_factorial.png
- grafica_memoria_factorial.png

### C
En C, las funciones equivalentes son:
- factorial_iterativo(int n) → cálculo mediante bucle for.
- factorial_recursivo(int n) → llamada recursiva con caso base.

Para la medición:
- Tiempo → clock() de <time.h>.
- Memoria → GetProcessMemoryInfo() de <psapi.h> (Windows).
- Se imprime directamente en consola una tabla con tiempo y memoria para cada 𝑛.

Archivo principal de ejecución:
C.c

## Guía para ejecutar el código
- Descargar el repositorio:
  
  git clone <URL_DEL_REPOSITORIO>

  cd <NOMBRE_DEL_REPOSITORIO>

- Ejecución en Python:
  Instalar dependencias:
  
  pip install -r requirements.txt

- Ejecutar:

  cd Python

  python medir_tiempo_memoria.py

Esto generará las gráficas y mostrará la tabla de resultados en consola.

### Ejecución en C (Windows)

- Compilar:

  cd C
  
  gcc  C.c -o factorial -lpsapi


- Ejecutar:

  ./factorial

La salida mostrará la tabla de tiempos y memoria en consola.

## Herramientas y Dependencias

### Python

- Python 3.6+

- Librerías:

  memory_profiler

  matplotlib

Instalación:

pip install -r requirements.txt

### C

- Compilador GCC (o compatible con C estándar).

- Librerías:

  <time.h>

  <windows.h>

  <psapi.h> (para medición de memoria en Windows).

## Resultados y Conclusiones

### Observaciones

- El método iterativo fue generalmente más eficiente en tiempo y memoria que el recursivo, especialmente para valores grandes de 𝑛.

- El método recursivo en Python presentó un incremento notable de uso de memoria debido a la pila de llamadas.

- En C, aunque el impacto de la recursividad fue menor que en Python, el método iterativo sigue siendo más estable y predecible.

### Conclusión

- Iterativo → mejor opción para cálculos factoriales grandes, más rápido y consume menos memoria.

- Recursivo → útil para ilustrar conceptos, pero poco práctico para valores altos debido a posibles desbordamientos de pila y mayor consumo de memoria.

- La comparación entre Python y C muestra que C es significativamente más rápido y consume menos memoria en general, lo que lo hace más adecuado para aplicaciones de alto rendimiento.


-Realizado por Alejandro Poveda Sandoval, fecha: 12/08/25.
