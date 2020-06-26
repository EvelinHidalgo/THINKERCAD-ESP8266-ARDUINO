**TUTORIAL PARA SIMULADOR EN THINKERCAD ARDUINO Y ESP82**

**ARDUINO UNO**

Arduino es una plataforma de creación de electrónica de código abierto, la cual está basada en hardware y software libre, flexible y fácil de utilizar para los creadores y desarrolladores. Esta plataforma permite crear diferentes tipos de microordenadores de una sola placa a los que la comunidad de creadores puede darles diferentes tipos de uso.
Arduino UNO es una placa basada en el microcontrolador ATmega328P. Tiene 14 pines de entrada/salida digital (de los cuales 6 pueden ser usando con PWM), 6 entradas analógicas, un cristal de 16Mhz, conexión USB, conector jack de alimentación, terminales para conexión ICSP y un botón de reseteo. Tiene toda la electrónica necesaria para que el microcontrolador opere, simplemente hay que conectarlo a la energía por el puerto USB o con un transformador AC-DC

**Caracterícas:**

•	Microcontrolador: ATmega328 

•	Voltaje de operación: 5V

•	Voltaje de entrada (recomendado): 7-12V 

•	Voltaje de entrada (límites): 6-20V 

•	Pines de E/S digitales: 14 (de los cuales 6 proporcionan salida PWM) 

•	Pines de entrada analógica: 6

•	Corriente DC por pin de E/S: 40 mA 

•	Corriente DC para 3.3V Pin: 50 mA

•	Memoria Flash: 32 KB de los cuales 0,5 KB utilizados por el bootloader 

•	SRAM: 2 KB (ATmega328) 

•	EEPROM: 1 KB (ATmega328) 

•	Velocidad de reloj: 16 MHz


**ESPECIFICACIONES ARDUINO UNO**

![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img1.jpg)

**1.Botón de reset:** Sirve para inicializar nuevamente el programa cargado en el microcontrolador de la placa. Cuando deje de responder el Arduino Uno es el botón de encendido o apagado para que vuelva a restablecerse. 

**2. Pines o puertos de entrada y salida:** son los pines donde conectar los sensores, componentes y actuadores que necesiten de señales digitales

**3. Pines o puertos de entrada y salida:** son los pines donde conectar los sensores, componentes y actuadores que necesiten de señales digitales.

**4.Puerto USB:** Utilizado tanto para conectar con un ordenador y transferir o cargar los programas al microcontrolador como para dar electricidad al Arduino. También se usa como puerto de transferencia serie a la placa, tanto para transmisión como para recepción de datos.

**5. Chip de interface USB:** es el encargado de controlar la comunicación con el puerto USB.

**6.Reloj oscilador:** es el elemento que hace que el Arduino vaya ejecutando las instrucciones. Es el encargado de marcar el ritmo al cual se debe ejecutar cada instrucción del programa.

**7. Led de encendido:** es un pequeño LED que se ilumina cuando la placa esta correctamente alimentada.

**8. Microcontrolador:** este es el cerebro de cualquier placa Arduino. Es el procesador que se encarga de ejecutar las instrucciones de los programas.

**9. Regulador de tensión:** este sirve para controlar la cantidad de electricidad que se envía a los pines, con lo que asegura que no se estropee lo que conectemos a dichos pines.

**10. Puerto de corriente continua:** este puerto es el que se usa para darle electricidad a la placa si no se usa alimentación USB.

**11. Zócalo de tensión:** aquí estarán los pines con los que alimentaremos nuestro circuito.

**12. Entradas analógicas:** zócalo con distintos pines de entrada analógica que permiten leer entradas analógicas.
POTENCIA

La placa puede funcionar con una alimentación externa de 6 a 20 voltios. Sin embargo, si se suministra con menos de 7V, la clavija de 5V puede suministrar menos de cinco voltios y la placa puede ser inestable. Si se utilizan más de 12V, el regulador de voltaje puede sobrecalentarse y dañar la placa. El rango recomendado es de 7 a 12 voltios.

**Pines de potencia**

•	VIN:El voltaje de entrada a la placa Arduino cuando está usando una fuente de alimentación externa (a diferencia de los 5 voltios de la conexión USB u otra fuente de alimentación regulada). Puede suministrar tensión a través de esta clavija o, si lo hace a través de la toma de corriente, acceder a ella a través de esta clavija. 

•	5V: Esta clavija emite un 5V regulado desde el regulador de la tarjeta. La tarjeta puede alimentarse ya sea desde el conector de alimentación de CC (7 – 12 V), el conector USB (5 V) o la clavija VIN de la tarjeta (7-12 V). La alimentación de tensión a través de las clavijas de 5V o 3,3V puentea el regulador y puede dañar la placa. 

•	3V3: Una alimentación de 3,3 voltios generada por el regulador de a bordo. El consumo máximo de corriente es de 50 mA.

•	GND: Pins de tierra.

**ENTRADA Y SALIDA, INPUT AND OUTPUT**

Cada uno de los 14 pines digitales de la Uno puede utilizarse como entrada o salida, utilizando las funciones pinMode(), digitalWrite() y digitalRead(). Funcionan a 5 voltios. Cada clavija puede proporcionar o recibir un máximo de 40 mA y tiene una resistencia pull-up interna (desconectada por defecto) de 20-50 kOhms. Además, algunos pines tienen funciones especializadas: 

•	Serial: 0 (RX) y 1 (TX). Se utiliza para recibir (RX) y transmitir (TX) datos en serie TTL. Estos pines están conectados a los pines correspondientes del chip Serial ATmega8U2 USB-to-TTL.

•	Interrupciones externas: 2 y 3. Estos pines pueden configurarse para activar una interrupción en un valor bajo, un flanco ascendente o descendente, o un cambio de valor. Vea la función attachInterrupt () para más detalles. 

•	PWM: 3, 5, 6, 9, 10 y 11. Proporciona salida PWM de 8 bits con la función analogWrite (). 

•	SPI: 10 (SS), 11 (MOSI), 12 (MISO), 13 (SCK). Estos pines soportan la comunicación SPI utilizando la biblioteca SPI. 

•	LED 13: Hay un LED incorporado conectado al pin 13 digital. Cuando la clavija es de valor ALTO, el LED se enciende, cuando la clavija es BAJA, se apaga. 

La Uno tiene 6 entradas analógicas, etiquetadas de A0 a A5, cada una de las cuales proporciona 10 bits de resolución (es decir, 1024 valores diferentes). Por defecto miden de tierra a 5 voltios, aunque es posible cambiar el extremo superior de su rango usando el pin AREF y la función analogReference(). 

**PINES TIENEN FUNCIONALIDAD ESPECIALIZADA**

•	TWI: Pin A4 o SDA y pin A5 o SCL. Soporta la comunicación TWI usando la biblioteca Wire.

•	AREF: Tensión de referencia para las entradas analógicas. Se utiliza con analogReference (). 

•	RESET: Lleve esta línea a un nivel BAJO para reiniciar el microcontrolador. Típicamente se usa para añadir un botón de reinicio a los escudos que bloquean el que está en la placa.

**DIAGRAMA PINOUT ARDUINO UNO**

![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img2.jpg)

**ARDUINO UNO PINOUT – FUENTE DE ALIMENTACIÓN **

Hay 3 formas de alimentar el Arduino Uno: 

•	Barrel Jack: El Barrel Jack, o DC Power Jack puede ser usado para alimentar tu placa Arduino. El conector cilíndrico suele estar conectado a un adaptador de pared. La tarjeta puede ser alimentada por 5-20 voltios, pero el fabricante recomienda mantenerla entre 7-12 voltios. Por encima de 12 voltios, los reguladores podrían sobrecalentarse, y por debajo de 7 voltios, podrían no ser suficientes.

•	VIN Pin: Este pin se utiliza para alimentar la placa Arduino Uno utilizando una fuente de alimentación externa. El voltaje debe estar dentro del rango mencionado anteriormente. 

•	Cable USB :cuando se conecta a la computadora, proporciona 5 voltios a 500mA.

![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img3.jpg)

Hay un diodo de protección de polaridad que se conecta entre el positivo de la clavija del barril y la clavija VIN, con una capacidad nominal de 1 amperio.

Cuando se alimenta un circuito a través de la toma de barril o VIN, la capacidad máxima disponible está determinada por los reguladores de 5 y 3.3 voltios a bordo del Arduino. 

•	5v y 3v3 Proporcionan 5 y 3.3v regulados para alimentar componentes externos de acuerdo con las especificaciones del fabricante. 

•	GND En el pinout de Arduino Uno, puedes encontrar 5 pines GND, todos ellos interconectados. 

Las clavijas GND se utilizan para cerrar el circuito eléctrico y proporcionar un nivel de referencia lógico común en todo el circuito. Asegúrate siempre de que todos los GNDs (del Arduino, periféricos y componentes) estén conectados entre sí y tengan una conexión a tierra común. 

•	RESET – reinicia el Arduino

•	IOREF – Este pin es la referencia de entrada/salida. Proporciona la referencia de tensión con la que funciona el microcontrolador.

**ARDUINO UNO PINOUT – ANALOG IN**

 La placa Arduino Uno tiene 6 pines analógicos, que utilizan ADC (Convertidor de Analógico a Digital). Estos pines sirven como entradas analógicas, pero también pueden funcionar como entradas o salidas digitales.
 
![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img4.jpg)

**Conversión de analógico a digital**

 ADC son las siglas de Analog to Digital Converter. El ADC es un circuito electrónico utilizado para convertir señales analógicas en señales digitales. Esta representación digital de señales analógicas permite al procesador, que es un dispositivo digital, medir la señal analógica y utilizarla durante su funcionamiento. 
Los pines Arduino A0-A5 son capaces de leer tensiones analógicas. En Arduino el ADC tiene una resolución de 10 bits, lo que significa que puede representar una tensión analógica de 1.024 niveles digitales. El ADC convierte el voltaje en bits que el microprocesador puede entender.

**ARDUINO UNO PINOUT – DIGITAL PINS**

•	Los pines 0-13 del Arduino Uno sirven como pines de entrada/salida digital.

•	El pin 13 del Arduino Uno está conectado al LED incorporado. 

•	En el Arduino Uno – los pines 3,5,6,9,10,11 tienen capacidad PWM.
 Es importante tener en cuenta: 
 
•	Cada clavija puede proporcionar hasta 40 mA máx. Pero la corriente recomendada es de 20 mA. 

•	La corriente máxima absoluta proporcionada de todos los pines juntos es de 200 mA.

![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img5.jpg)

**THINKERCAD**

TinkerCAD es una colección online que incluye herramientas de software de Autodesk que permite a los principiantes crear modelos 3D. Este software CAD se basa en una geometría sólida constructiva (CSG), que permite a los usuarios crear modelos complejos mediante la combinación de objetos más simples. Como resultado, este software de modelado 3D es fácil de usar y actualmente es disfrutado por muchos, particularmente maestros, niños, aficionados y diseñadores. Además, es gratis.
TinkerCAD es una buena alternativa a otro software de modelado 3D como SketchUp o Fusion360, otra solución de Autodesk, si no necesita las opciones más avanzadas de estas soluciones. En realidad, la compañía líder de software adquirió TinkerCAD en 2013, dos años después de su lanzamiento por el ex ingeniero de Google Kai Backman y su cofundador Mikko Mononen. La principal ventaja sobre estos dos programas es que es gratuito y, sin embargo, ofrece más libertad de modelado de lo que parece.

![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img6.png)

**Tinkercad ofrece:**

•	Aplicación de diseño e impresión 3D

•	Simulador de circuitos, incluido Arduino

•	Diseños 3D interactivos con electrónica:

•	Publicar nuestro proyectos

•	Ver otros proyectos y clonarlos.

**Tinkercad Circuits**

Herramienta online gratuita de Autodesk que permite dibujar esquemas de forma similar a Fritzing. Además permite simulación de circuitos, e incluso podemos realizar la “programación virtual” de las placas Arduino y comprobar el funcionamiento, es un simulador online.
Una herramienta muy interesante que ofrece Tinkercad Circuits es el debugger, con ella se puede parar la ejecución de un programa y ver los valores de las variables, algo que con arduino no podemos hacer. Permite “parar” el tiempo.
Los montajes de circuitos son simples circuitos pre-fabricados que se pueden incorporar en tus diseños 3D. Cuando descargues tu diseño para imprimir, los componentes electrónicos no se exportarán, pero si los cortes que creer para introducirlos. Esto significa que puedes crear un diseño con todo lo necesario sin tener que eliminar los componentes antes de imprimir.

**ESP8266**

ESP8266 es un puente de puerto serie a WiFi, incluye un microcontrolador para manejar el protocolo TCP/IP y el software necesario para la conexión 802.11, la mayoría de modelos dispone de entradas/salidas (I/O) digitales y algunos modelos una entrada analógica al igual que otros microcontroladores, su punto fuerte es disponer de acceso WIFI y por su bajo precio el chip ESP8266 parece destinado a dar un gran empujón a lo que se ha llamado Internet de las cosas.
ESP8266 se puede programar usando el lenguaje interpretado Lua en entornos como ESPlorer, y el IDE y lenguaje de Arduino Processing/Wiring.

**Módulo WiFi ESP8266**

ESP8266 es un módulo de sistema en chip (SoC) habilitado para Wi-Fi desarrollado por el sistema Espressif. Se utiliza principalmente para el desarrollo de aplicaciones integradas de IoT (Internet de las cosas).

![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img7.jpg)

**Módulo WiFi ESP8266-01**

ESP8266 viene con capacidades de:

•	Wi-Fi de 2.4 GHz (802.11 b / g / n, compatible con WPA / WPA2),

•	Entrada / salida de propósito general (16 GPIO),

•	Protocolo de comunicación en serie del circuito integrado (I²C),

•	Conversión de analógico a digital (ADC de 10 bits)

•	Protocolo de comunicación en serie de la interfaz periférica en serie (SPI),

•	Interfaces I²S (Inter-IC Sound) con DMA (Acceso directo a memoria) (compartir pines con GPIO),

•	UART (en pines dedicados, más un UART de solo transmisión se puede habilitar en GPIO2), y
modulación de ancho de pulso (PWM).

Emplea una CPU RISC de 32 bits basada en el Tensilica Xtensa L106 que funciona a 80 MHz (o overclockeado a 160 MHz). Tiene una ROM de arranque de 64 KB, RAM de instrucciones de 64 KB y RAM de datos de 96 KB. Se puede acceder a la memoria flash externa a través de SPI.
El módulo ESP8266 es un transceptor inalámbrico independiente de bajo costo que se puede usar para desarrollos de IoT de punto final.
Para comunicarse con el módulo ESP8266, el microcontrolador necesita usar un conjunto de comandos AT. El microcontrolador se comunica con el módulo ESP8266-01 utilizando UART con una velocidad de transmisión especificada.

Hay muchos fabricantes de terceros que producen diferentes módulos basados en este chip. Entonces, el módulo viene con diferentes opciones de disponibilidad de pin como:

•	ESP-01 viene con 8 pines (2 pines GPIO) - Antena de rastreo de PCB. (se muestra en la figura anterior)

•	ESP-02 viene con 8 pines, (3 pines GPIO) - Conector de antena U-FL.

•	ESP-03 viene con 14 pines, (7 pines GPIO) - Antena de cerámica.

•	ESP-04 viene con 14 pines, (7 pines GPIO) - Sin hormiga.

Por ejemplo, la figura siguiente muestra los pines del módulo ESP-01
Descripción del pin del módulo ESP8266-01

![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img8.png)

**Pines del módulo ESP8266-01**

3V3 : - Pin de alimentación de 3,3 V.

GND : - Pin de tierra.

RST : - Pin de restablecimiento bajo activo.

ES : - Pin de habilitación alta activa.

TX : - Pin de transmisión en serie de UART.

RX : - Pin de recepción en serie de UART.

GPIO0 y GPIO2 : - Pines de E / S de uso general. Estos pines deciden en qué modo (arranque o normal) se inicia el módulo. También decide si los pines TX / RX se usan para programar el módulo o para propósitos de E / S en serie.
Para programar el módulo usando UART, conecte GPIO0 a tierra y GPIO2 a VCC o déjelo abierto. Para usar UART para E / S en serie normales, deje ambos pines abiertos (ni VCC ni tierra).


**MANUAL DE USUARIO**

1.Ingresar en el siguiente link https://www.tinkercad.com/dashboard.Click en circuitos.

![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img9.png)

2. Click en crear nuevo circuito.
![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img10.png)

3.Click en buscar y escribir Módulo Wifi, arrastrar el componente hasta la ventana de ejercución.
![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img11.png)

4.Click en buscar y escribir Arduino, arrastrar el componente hasta la ventana de ejercución.
![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img12.png)

5.Click en buscar y escribir Placa de prueba pequeña, arrastrar el componente hasta la ventana de ejercución.
![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img13.png)

6.Click en buscar y escribir Resistor, arrastrar el componente hasta la ventana de ejercución, en este caso serían cinco resistencias
![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img14.png)

7.Click en buscar y escribir LED, arrastrar el componente hasta la ventana de ejercución, en este caso dos leds.!
![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img15.png)

8.Al tener todos los componentes necesarios en la ventana se empezará a unir los puertos tanto del SPE8166 y del Arduino como se menciona a continuación.
Arduino puerto 2 con SPE8166 puerto TX

Arduino puerto 4 con Resistencia 4

Arduino puerto 7 con Resistencia 5

Arduino 3.3V con Resistencia 1 

Arduino GND con Resistencia 3

Arduino GND con Led 1 y 2
![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img16.png)
![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img17.png)
![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img18.png)
![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img19.png)

9.En la parte derecha click en el ícono Código-Texto .
![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img20.png)
![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img21.png)

10.Se abrirá una pequeña ventana a la derecha donde se tendrá que ingresar el código para que realice la simulación Thinkercad.
![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img22.png)
![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img23.png)
![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img24.png)

11.Finalmente se obtiene la simulación.

![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img25.png)
![](https://github.com/EvelinHidalgo/THINKERCAD-ESP8266-ARDUINO/blob/master/img/img26.png)
**BIBLIOGRAFÍA**

[1] Descubre Arduino.com.(2014). ARDUINO UNO, PARTES, COMPONENTES, PARA QUÉ SIRVE Y DONDE COMPRAR.Recuperado de:https://descubrearduino.com/arduino-uno/

[2]Ortega & Gasset.(2020).enerxia.net.PROTEUS(ARES e ISIS)Control de GPIO con Python en Raspberry Pi.Recuperado de: https://www.enerxia.net/portal/index.php?option=com_content&view=article&id=406:electronica-proteus-
[3]Valle.(2020). ESP8266 todo lo que necesitas saber del módulo WiFi para Arduino
.Recuperado de: https://programarfacil.com/podcast/esp8266-wifi-coste-arduino/

[4] Alicia,M.(2020). TinkerCAD: ¡Te contamos todo lo que necesitas saber!
.Recuperado de: https://www.3dnatives.com/es/tinkercad-software-200420202/

