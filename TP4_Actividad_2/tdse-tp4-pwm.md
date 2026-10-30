# tdse-tp4-pwm

1. Forkear el repositorio y abrir el proyecto en STM32CubeIDE
2. Analizar en el IOC las configuraciones del TIM3 y del RCC, sin modificarlas
3. En PA6 colocar un cable Dupont hembra macho y dejarlo al aire. En GND colocar un cable Dupont macho macho y dejarlo al aire.
4. Enchufar la placa NUCLEO-F103RB

## Test 1
5. Volver al código y configurar el primer test, verificando el `#define TEST_NUMBER` (línea 18 de app.c), es decir que diga `#define TEST_NUMBER TEST_1`
6. Compilar y debuggear.
7. Colocar la punta del osciloscopio entre PA6 y GND y analizar la forma de onda mostrada. ¿Cuál es el período de la señal? ¿Se modifica? ¿Cómo se define duty cycle? Se modifica?
8. Colocar un led entre PA6 y GND (no olvidar R de polarización) y observar la intensidad del brillo.

La señal es una onda cuadrada con frecuencia fija, el cual es 1 KHz, y período de 159 us, pero cuyo duty cycle varía con el tiempo.
En aproximadamente 2,5 segundos se efectua un barrido de dutycycle de 0% a 100%.
Al colocar el led, se ve como cambia su intensidad de brillo de acuerdo al barrido del duty cycle.

## Test 2
9. Volver al código y configurar el segundo test, mediante la directiva `#define TEST_NUMBER TEST_2`
10. Compilar y debuggear.
11. Colocar la punta del osciloscopio entre PA6 y GND y analizar la forma de onda mostrada. ¿Qué ocurre con el período de la señal? ¿Qué ocurre con el duty cycle?
12. Colocar un led entre PA6 y GND (no olvidar R de polarización) y observar la intensidad del brillo.
13. Comparar resultados

Lo que pasa hace ahora es que cambia de 2.5kHz a 4 kHz, manteniendo el dutycycle constante.
Esto hace que se vea como si estuviera prendido siempre, con un ligero tintineo(Oscilación). 

