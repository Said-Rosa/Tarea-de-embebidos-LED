# Tarea-de-embebidos-LED

Tarea de STM32 (BlackPill STM32F401CCU6) simulada en Proteus, hecha sobre el proyecto de clase.

- LED3 parpadea cada 2 s con la interrupción del TIM1 (contador de 20 interrupciones de 100 ms).
- LED5 (PB1) se enciende y apaga por comandos serie desde Hercules a través del COMPIM (USART1, 9600 baudios):
  - `LED5=on*` enciende el LED5
  - `LED5=off*` apaga el LED5

## Archivos

- `bollo.ioc`: configuración de CubeMX.
- `Core/Src/main.c`: función `procesa_rx()` y su llamada en el `while(1)`.
- `Core/Src/librerias/`: librerías UART del profesor.
- `BOLLO.pdsprj`: circuito de Proteus. Usa el programa `build/Debug/bollo.elf`.

## Compilar

Con CMake (presets de STM32CubeMX): `cmake --preset Debug` y `cmake --build build/Debug`.
