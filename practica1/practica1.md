# Misión 1: Reconocimiento de Equipos y Espectro
Integrantes de grupo:
* Daniel Ricardo Guerrero Cruz
* Luis Arley Martinez Caballero
## Fase 1: Exploración y Descubrimiento (El Ojo Panorámico del SDR)
1. Mapeo del Terreno: Conecta la antena al SDR. Utiliza el software para realizar un barrido amplio del espectro. (50 a 2200 MHz)

2. Identificación de Objetivos: Observa la visualización en cascada (waterfall) e identifica al menos tres señales comerciales potentes. El SDR es tu herramienta de "visión amplia" para encontrar rápidamente puntos de interés.

3. Selección de un Objetivo: Elige una de esas señales (la más clara y estable) para un análisis más profundo. Anota su frecuencia central aproximada.

Evidencia: 
* Captar la señal mas potente del espectro radioelectrico en el laboratorio, tomarle una captura de pantalla y adjuntar la evidencia.
* Describa brevemente los servicios encontrados en el barrido.
--------------------------------------------------------------------
 
Se encontraron dos emisoras de radio ubicadas en las frecuencias 99.7 MHz y 103.7 MHz, la primera corresponde a la FM mientras la segunda corresponde a El Sol, siendo esta ultima la mas potente observada, tambien se encontró una señal de servicio móvil ubicada en los 900 MHz, a diferencia de las señales de radio esta tenia un ancho de banda mas estrecho evidenciado por la visualización en cascada que muestra una linea delgada. A demás de estas señales que fueron las que mas nos llamaron la atención, también se encontraban otras emisoras como la 90.7 correspondiente a W Radio o la 96.9 correspondiente a la UIS estéreo.

 <img width="1920" height="1080" alt="103_7" src="https://github.com/user-attachments/assets/7fde7146-40a0-414b-8fde-34c887dfb7db" />

--------------------------------------------------------------------

## Mision 1 Fase 2: Análisis de Precisión (La Lupa del Analizador)
1. Enfoque: Conecta la antena al Analizador de Espectro.

2. Configuración Fina: Sintoniza el analizador a la frecuencia central que encontraste con el SDR. Ajusta el SPAN para "hacer zoom" en la señal y el RBW para obtener una mejor resolución.

3. Recolección de datos (Dominio de la Frecuencia): Mide y registra con precisión:

* Frecuencia Central: La frecuencia exacta del pico de la portadora.

* Potencia: La potencia máxima de la señal en dBm.

* Ancho de Banda: El ancho de banda que ocupa la señal (use dos marcadores)

* Resolución de ancho de banda (RBW): defina la mejor estrategia para estudiar su señal y registre su elección.

* SPAN: Defina la mejor estrategia desde su experiencia para observar la señal completamente.

Evidencia: 
* Guarda una captura de pantalla del espectro con los marcadores de medición visibles.
* Describa el proceso de eleccion de los principales parametros del analizador de espectro para el estudio de esta señal
--------------------------------------------------------------------

Frecuencia Central: 103.7 MHz
Potencia: -53 dBm
Ancho de Banda: 270 kHz
Resolución de ancho de banda (RBW): 50 kHz
SPAN: 6 MHz

Para realizar el estudio de esta señal se estableció una frecuencia central de 103.7 MHz con el objetivo de encontrarnos con la misma señal visualizada en GNU radio. Posterior a esto, se configuró el SPAN a 6 MHz, lo suficiente como para visualizar el espectro tanto de la emisora como de otras señales cercanas y poder medir el ancho de banda utilizando la regla de los 20 dB. Se utilizaron marcadores para determinar que la potencia maxima es de -53 dBm, por lo tanto, el ancho de banda es igual al rango de frecuencias para los cuales se alcanza un valor cercano a -73 dBm.

![emisora_en_analizador_de_espectro](https://github.com/user-attachments/assets/19dfc50b-cf75-4389-80f3-adc03429bd30)

--------------------------------------------------------------------

## Mision 1 fase 3. Visualización de la Onda
1. Conexión: Conecta la antena a la entrada del osciloscopio.

2. Captura de la Forma de Onda: Esta es la parte más desafiante. Deberás ajustar la relación de la sonda de medida, la escala vertical (Volts/div) y la base de tiempo (s/div) para intentar "capturar" y estabilizar la forma de onda de la señal de RF. Activa el modo de disparo (Trigger) en el canal de entrada para estabilizar la visualización.

3. Recolección de Inteligencia (Dominio del Tiempo): Una vez tengas una forma de onda visible:

* Mide su frecuencia usando los cursores o las mediciones automáticas.

* Mide su voltaje pico a pico (Vpp).

Evidencia: 
* Guarda una captura de pantalla de la forma de onda visualizada en el osciloscopio, esta medición deberá apoyarse en el análisis de la FFT.
* Describa la señal observada en el oscilocopio ¿Cuales caracteristicas pudo observar o fueron mas evidentes?
--------------------------------------------------------------------

Frecuencia: 32 MHz
Vpp: 27 mV

Al igual que en las primeras dos fases de la misión nos enfocamos en la señas ubicada en 103.7 MHz, la localizamos activando el FFT en el osciloscopio. Las mediciones se consiguieron presionando el botón "Meas" y eligiendo la opción "medida" en la pantalla táctil.
La señal varia mucho en su frecuencia, el valor medio medido usando el osciloscopio fue de 32 MHz, pero en realidad se observan valores que cambian continuamente entre 0 y 100 MHz. La señal está en el rango de decenas de milivoltios pico a pico según la medición, y esta tensión se mantuvo bastante estable en comparación a la medición de frecuencia, variando entre 21 mV y 30 mV.

![frec_act3_lab1](https://github.com/user-attachments/assets/8f9231da-1348-42ab-86a0-9cf685ad2dd7)

--------------------------------------------------------------------
## Entregables y Análisis del Reporte:

## Resultados y Hallazgos: 
Presente un párrafo comparando las mediciones de frecuencia obtenidas con los tres equipos (SDR, Analizador y Osciloscopio). 

Incluya las capturas de pantalla de cada fase, debidamente etiquetadas. 

## Análisis y Discusión: 
Comparativa de Equipos: ¿Con cuál equipo le fue más fácil encontrar la señal? ¿Qué ventajas y desventajas tiene cada equipo para esta tarea de reconocimiento? 

Precisión: ¿Cuál de los tres equipos ofrece la medida de frecuencia más confiable y precisa? ¿Por qué cree que es así? 

La Conexión Tiempo-Frecuencia: Explique con sus propias palabras qué representa el "pico" que se observa en el analizador de espectro en relación con la onda sinusoidal que se observa en el osciloscopio. 

Desafíos: Describa las dificultades que se encuentran, especialmente al intentar visualizar la señal en el osciloscopio, y cómo la resuelve.

---------------------------------------------------------------------

Comparativa de Equipos

SDR: Fue el más sencillo para localizar la señal, ya que la visualización en cascada facilita la identificación de picos y su evolución en el tiempo. Sin embargo, su precisión en frecuencia depende del hardware del receptor y puede presentar ligeras desviaciones.

Analizador de Espectro: Ofreció la medida más clara y confiable de la frecuencia central, con un pico definido y un ancho de banda bien delimitado, es el más preciso para tareas de caracterización espectral.

Osciloscopio: Aunque permite observar la forma de onda en el tiempo y realizar FFT, su sensibilidad y resolución en frecuencia son menores frente a un analizador dedicado.

Precisión: El analizador de espectro proporciona la medida de frecuencia más confiable y precisa, ya que está diseñado específicamente para este tipo de mediciones. Su resolución y calibración superan a las del SDR y al osciloscopio, que dependen más de configuraciones y ajustes.

Conexión Tiempo-Frecuencia: Consideramos que el pico en el analizador de espectro representa la la frecuencia fundamental de la señal. En el osciloscopio, esta misma señal aparece como una onda sinusoidal de muy alta frecuencia. En otras palabras, el pico en frecuencia es la versión espectral de la onda rápida que vemos en el tiempo.

Desafíos: La principal dificultad surgió al visualizar la señal en el osciloscopio, ya que al tratarse de una frecuencia elevada (103.7 MHz) se requería ajustar correctamente la pantalla poder visualizarla, la baja amplitud de la señal obligó a optimizar la escala vertical y usar promedios para reducir el ruido. También fue necesario probar las diferentes herramientas y botones disponibles en el osciloscopio con el objetivo de medir la tension pico a pico y la frecuencia de manera precisa

<img width="1920" height="1080" alt="Captura desde 2025-08-20 17-43-38" src="https://github.com/user-attachments/assets/47097905-ecf0-43fd-bc10-78df85a52877" />
<img width="1920" height="1080" alt="Captura desde 2025-08-20 17-42-57" src="https://github.com/user-attachments/assets/60470671-14ec-4932-843a-91a0715aa70c" />
<img width="1920" height="1080" alt="Captura desde 2025-08-20 17-42-28" src="https://github.com/user-attachments/assets/db04581c-187b-4b20-ad4d-4d082a6f89f2" />
<img width="1920" height="1080" alt="Captura desde 2025-08-20 17-41-12" src="https://github.com/user-attachments/assets/a30ec5fa-2787-428a-ab9a-de74dc9fe321" />

-----------------------------------------------------------------------

### Resuma el rol estratégico de cada instrumento: el SDR para explorar, el Analizador para medir en frecuencia y el Osciloscopio para analizar en el tiempo.

En las pruebas realizadas, se observó la misma señal de radio en torno a los 103.7 MHz utilizando tres equipos distintos: SDR, analizador de espectro y osciloscopio digital. En el SDR se pudo identificar la frecuencia de manera rápida gracias a la interfaz gráfica. Con el analizador de espectro, la frecuencia central de la señal se midió con mayor exactitud, mostrando un pico definido en 103.7 MHz. Finalmente, con el osciloscopio, aunque se visualizó la señal tanto en el dominio del tiempo como en frecuencia mediante la función FFT, el proceso fue más complejo debido a la necesidad de configurar adecuadamente el span y la resolución espectral.



El SDR asumió un rol muy útil en la exploración de las señales captadas por la antena gracias a la interfaz visual presente en GNU Radio, resulta muy comodo utilizar el slider para encontrar las señales mas fuertes que destacan por su espectro de mayor grosor e intensidad de color.

El analizador de espectro resultó especialmente útil para características de la señal como la potencia, y el ancho de banda, siempre y cuando estén bien configurados los parámetros de frecuencia central, Span, y RBW.

El osciloscopio también proporciona una ventana para visualizar el espectro de las señales, pero es mas limitada e incómoda de usar debido a que comparte pantalla con la visualización en el dominio del tiempo. Es mejor usar este instrumento para observar la señal senoidal captada.
