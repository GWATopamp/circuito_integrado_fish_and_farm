<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works
El circuito recibe 4 bits de entrada: A y B codifican el nivel de consumo actual (00=reposo, 01=normal, 10=pico, 11=sobrecarga) y T1 y T0 definen el umbral de alarma. Un decodificador 2 a 4 (one-hot) enciende únicamente el LED correspondiente al nivel medido. Paralelamente, un comparador digital de magnitud evalúa si el nivel (A,B) es estrictamente mayor que el umbral (T1,T0) y, en caso afirmativo, activa la señal de alarma.

## How to test
Aplicar las 16 combinaciones posibles de las entradas A, B, T0 y T1 mediante interruptores externos. Para cada combinación, verificar que solo un LED de nivel (LED1 a LED4) se encienda según la codificación de A y B, y que la salida de alarma se active únicamente cuando el valor binario (A,B) sea superior a (T1,T0), donde A y T1 son los bits más significativos.

## External hardware
4 interruptores (switches) para fijar los valores de A, B, T0 y T1; 4 LEDs para visualizar los niveles de consumo (LED1 a LED4); 1 LED adicional para la señal de alarma.
