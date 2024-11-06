Cubo LED 8x8x8 con ATmega8
Descripción

Este proyecto consiste en la construcción de un cubo LED 8x8x8 controlado por un microcontrolador ATmega8. Se utilizaron registros de desplazamiento 74HC595 y transistores ULN2803 para controlar los cátodos de cada piso. A continuación, se describe el proceso de construcción, los materiales utilizados y cómo replicar el proyecto.
=======
Este proyecto consiste en la construcción de un cubo LED 8x8x8 controlado por un microcontrolador ATmega8. Utilicé registros de desplazamiento 74HC595 y transistores ULN2803 para controlar los cátodos de cada piso. A continuación, se describe el proceso de construcción, los materiales utilizados y cómo replicar el proyecto.



Materiales
•	1x ATmega8
•	9x Registros de desplazamiento 74HC595
•	1x Transistor ULN2803
•	512x LEDs (preferiblemente del mismo color o combinaciones de colores)
•	66x Resistencias de 220Ω (para limitar la corriente de los LEDs)
•	PCB Baquelita universal perforada de 90 cm x 15 cm
•	9x Socket de 16 pines para cada compuerta 74HC595
•	Cables de conexión (suficientes para el proyecto)
•	1x Fuente de alimentación de 5V (preferiblemente de celular; no debe superar los 2 amperios de consumo)
•	1x Rollo de alambre galvanizado
•	2x Pines header hembra
•	2x Pines header macho
•	1x Cristal de 16 MHz
•	2x Capacitores de 22 pF
•	2x Resistencias de 10 kΩ
•	3x Pulsadores sencillos (o los necesarios según el diseño)
•	1x Capacitor de 470 µF a 10V
•	1x Socket de 28 pines para el microcontrolador
•	1x Socket de 18 pines para el array de transistores
•	1x LED rojo
•	1x LED verde
Código Arduino
Puedes encontrar el código en la carpeta <Cub0_INO>.
## Materiales

- 1x ATmega8
- 9x Registros de desplazamiento 74HC595
- 1x Transistores ULN2803
- 512x LEDs (preferiblemente del mismo color o combinaciones de colores)
- 68x Resistencias de 220Ω (para limitar la corriente de los LEDs)
- xPCB Baquela universal perforada 90cm x 15cm
- 9x socket de 16pines para cada Compuerta 74hc595
- Cables de conexión (Bastantes jejej..)
- 1x Fuente de alimentación de 5V (Puede ser de Celular est no superara los 2 amperios de cosumo)
- 1x Rollo Alambre Galvanizado
- 2x Pines Header Hembra 
- 2x Pines Header Macho
- 1x Cristal 16mhz
- 2x Capitores 22pf
- 2x Resistencias 10kohm
- 3x Pulsadores sencillo (o de acuerdo a la nececidad)
- 1x Capacitor 470uf x 10v
- 1x socket 28pines para el microcontrolador
- 1x socket de 18pines para el array de transistores
- 1x Led Rojo
- 1x Led Verde

## CODIGO ARDUINO 

- Lo encuentras en la carpeta <Cub0_INO>

Esquema del Circuito

Construcción
1. Montaje de la Estructura del Cubo
• Preparar los LEDs: Organiza los LEDs en 8 capas de 8x8.
• Soldadura: Solda los ánodos de cada fila juntos y conecta los cátodos de cada columna de LEDs en cada piso.
• Cableado de los cátodos: Cada capa (piso) debe conectarse a un transistor ULN2803 para ser controlada.

2. Conexión del Circuito
• Conectar los registros de desplazamiento 74HC595: Estos controlarán las columnas de LEDs a través de las resistencias limitadoras.
• Conectar el ULN2803: Los cátodos de cada piso están controlados por los transistores ULN2803, los cuales son activados por las salidas del ATmega8.

3. Programación del Microcontrolador
El código fuente para controlar el cubo se encuentra en el archivo Cub0_INO.ino. Este código incluye secuencias animadas de encendido y apagado de los LEDs, las cuales pueden ser modificadas a voluntad.

Pasos para compilar y cargar el código al ATmega8:
• Conecta el ATmega8 a tu computadora utilizando una placa Arduino Uno.
• Abre el archivo .ino en el IDE de Arduino.
• Configura el IDE para usar el microcontrolador ATmega8 seleccionándolo en el menú "Herramientas".
• Carga el código en el ATmega8.

NOTA: Si no aparecen las placas MiniCore, utiliza el siguiente JSON, reinicia tu IDE y las librerías se actualizarán:
https://mcudude.github.io/MiniCore/package_MCUdude_MiniCore_index.json

4. Alimentación
El cubo se alimenta con una fuente de 5V. Asegúrate de que la fuente pueda entregar la corriente suficiente para alimentar todos los LEDs. El consumo total, con todos los LEDs encendidos, es de aproximadamente 1 a 1.5 amperios, dependiendo de los LEDs utilizados.

YouTube
Puedes ver el video del proyecto en el siguiente enlace:
https://youtu.be/N4tvsjkCFxY?feature=shared

