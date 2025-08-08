# tarea-1
-Comparación de eficiencia de algoritmos para calcular factoriales

-Propósito
Este proyecto compara dos enfoques diferentes (recursivo e iterativo) para calcular el factorial de un número entero. El objetivo es analizar y comparar su eficiencia en términos de tiempo de ejecución y uso de memoria.


-Implementación
*Se implementaron dos funciones en Python y C.
*facto_r(n) → Recursiva.
*facto_i(n) → Iterativa.

-Medición
-Python:
  -Tiempo: módulo `time`
  -Memoria: módulo `memory_profiler`
-C:
  -Tiempo: `clock()` de `time.h`
  -Memoria: herramienta `valgrind` con `massif`

Resultados:
-Iterativa más rápida y usa menos memoria para valores grandes.
-Recursiva puede generar `RecursionError` en Python por límite de profundidad.

-Cómo correr:
Python:
bash
pip install memory_profiler matplotlib
python graficas.py

-C:
gcc main.c -o factorial
./factorial

-Realizado por Alejandro Poveda Sandoval, fecha: 8/08/25.