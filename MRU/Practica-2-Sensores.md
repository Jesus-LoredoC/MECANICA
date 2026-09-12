# Práctica 1: Velocímetro con 2 sensores ultrasónicos

## Objetivo

Desarrollar un sistema capaz de medir la velocidad de una pelota pequeña utilizando dos sensores ultrasónicos colocados a una distancia conocida.

El sistema detecta el paso de la pelota en dos puntos diferentes y utiliza el tiempo transcurrido entre ambas detecciones para calcular su velocidad.

## Materiales

- 1 Arduino
- 2 sensores ultrasónicos HC-SR04
- 3 protoboards
- Cables de conexión
- 1 pelota pequeña
- 1 canaleta
- 1 computadora
- 1 cable USB para conectar el Arduino

## Fundamento

La velocidad de un objeto puede calcularse utilizando la distancia que recorre y el tiempo que tarda en recorrerla.

La fórmula utilizada es:

*Velocidad = Distancia / Tiempo*

Donde:

- *Velocidad* corresponde a la velocidad de la pelota.
- *Distancia* corresponde a la separación entre los puntos donde se realizan las detecciones.
- *Tiempo* corresponde al tiempo que tarda la pelota en desplazarse entre dichos puntos.

## Procedimiento

Para realizar esta práctica se siguieron los siguientes pasos:

### 1. Preparación de los materiales

Primero se reunieron todos los materiales necesarios para realizar la práctica: la placa Arduino, los dos sensores ultrasónicos HC-SR04, las tres protoboards, los cables de conexión, la pelota pequeña y la canaleta.

### 2. Programación de la placa Arduino

Se programó la placa Arduino utilizando el código que se nos proporcionó para realizar la práctica.

El programa se encargó de recibir las señales de los sensores y realizar las mediciones necesarias para determinar el tiempo que tardaba la pelota en pasar de un sensor al otro.

### 3. Configuración del rango de detección

Se dejó el radio o rango de detección de los sensores en el valor que ya se encontraba predispuesto en el programa proporcionado.

No se realizaron modificaciones a este parámetro, ya que se trabajó con la configuración establecida para la práctica.

### 4. Colocación de la canaleta

Se colocó la canaleta sobre una superficie estable para proporcionar una trayectoria definida para la pelota pequeña.

La canaleta permitió que la pelota siguiera un recorrido establecido y pasara frente a los sensores durante las pruebas.

### 5. Colocación de los sensores

Se colocaron los dos sensores ultrasónicos en diferentes puntos de la canaleta.

La distancia entre los sensores se estableció de acuerdo con las condiciones indicadas para la práctica, ya que esta distancia es necesaria para realizar posteriormente el cálculo de velocidad.

### 6. Conexión de los sensores a las protoboards

Los sensores ultrasónicos fueron conectados a las protoboards utilizando cables de conexión.

Posteriormente, se conectaron las protoboards con la placa Arduino, de manera que los sensores pudieran recibir alimentación eléctrica y enviar sus señales a los pines correspondientes del Arduino.

### 7. Conexiones eléctricas

Las conexiones utilizadas para los sensores ultrasónicos HC-SR04 fueron las siguientes:

| HC-SR04 #1 | Arduino | HC-SR04 #2 | Arduino |
|------------|---------|------------|---------|
| VCC | 5V | VCC | 5V |
| GND | GND | GND | GND |
| Trig | Pin 9 | Trig | Pin 11 |
| Echo | Pin 10 | Echo | Pin 12 |

De esta manera, cada sensor quedó conectado a sus respectivos pines de alimentación, disparo y recepción de señal.

### 8. Conexión de la placa Arduino

Una vez conectados los sensores a las protoboards, se conectaron los cables correspondientes desde la placa Arduino hacia las protoboards.

Se revisaron las conexiones antes de realizar las pruebas para comprobar que los sensores estuvieran correctamente alimentados y conectados a los pines establecidos.

### 9. Prueba del sistema

Después de realizar las conexiones y cargar el programa, se comprobó que los sensores detectaran correctamente la pelota.

Se verificó que la información obtenida por los sensores fuera recibida correctamente por el Arduino.

### 10. Realización de las mediciones

Se colocó la pelota pequeña en la parte inicial de la canaleta y se dejó avanzar.

Cuando la pelota pasó frente al primer sensor, el Arduino registró el momento de la primera detección.

Posteriormente, cuando la pelota pasó frente al segundo sensor, se registró la segunda detección.

### 11. Cálculo de la velocidad

Con los tiempos registrados por el Arduino se determinó el tiempo transcurrido entre ambas detecciones.

Posteriormente, utilizando la distancia conocida entre los sensores, se calculó la velocidad de la pelota mediante la fórmula:

*Velocidad = Distancia / Tiempo*

### 12. Repetición de las pruebas

Finalmente, se realizaron varias pruebas para comprobar el funcionamiento del sistema y obtener diferentes mediciones de velocidad.

## Resultados

Los resultados obtenidos durante las pruebas se pueden registrar en la siguiente tabla:

| Prueba | Distancia | Tiempo | Velocidad |
|--------|-----------|--------|-----------|
| 1 | [_] cm | [_] s | [_] cm/s |
| 2 | [_] cm | [_] s | [_] cm/s |
| 3 | [_] cm | [_] s | [_] cm/s |

---

# Práctica 2: Velocímetro con 3 sensores infrarrojos

## Objetivo

Desarrollar un sistema capaz de detectar el desplazamiento de una pelota pequeña utilizando sensores infrarrojos y registrar los tiempos correspondientes a su paso por diferentes puntos de la canaleta.

## Materiales

- 1 Arduino
- 3 sensores infrarrojos de barrera
- 3 protoboards
- Cables de conexión
- 1 pelota pequeña
- 1 canaleta
- 1 computadora
- 1 cable USB para conectar el Arduino

## Fundamento

Los sensores infrarrojos de barrera permiten detectar el paso de la pelota mediante una señal digital.

Al colocar los sensores en diferentes puntos de la canaleta, el Arduino puede registrar el momento en que la pelota interrumpe la barrera de cada sensor.

Con los tiempos registrados y las distancias conocidas entre los sensores es posible calcular la velocidad de la pelota.

La fórmula utilizada es:

*Velocidad = Distancia / Tiempo*

## Procedimiento

### 1. Preparación de los materiales

Primero se reunieron los materiales necesarios para realizar la práctica: la placa Arduino, los tres sensores infrarrojos de barrera, las tres protoboards, los cables de conexión, la pelota pequeña y la canaleta.

### 2. Programación de la placa Arduino

Se programó la placa Arduino utilizando el código que se nos proporcionó para realizar la práctica.

El programa permitió recibir las señales digitales provenientes de los sensores infrarrojos y registrar los momentos en que la pelota era detectada.

### 3. Configuración del rango de detección

Se dejó el rango de detección de los sensores en el valor que ya se encontraba predispuesto para la práctica.

Se trabajó con la configuración proporcionada, sin modificar el rango establecido.

### 4. Colocación de la canaleta

Se colocó la canaleta sobre una superficie estable para proporcionar una trayectoria definida para la pelota pequeña.

### 5. Colocación de los sensores

Los sensores infrarrojos fueron colocados en diferentes puntos de la canaleta para detectar el paso de la pelota durante su recorrido.

La separación entre los sensores permitió obtener diferentes puntos de referencia para realizar las mediciones.

### 6. Conexión de los sensores a las protoboards

Los sensores infrarrojos fueron conectados a las protoboards mediante cables.

Posteriormente, las protoboards fueron conectadas a la placa Arduino para proporcionar alimentación eléctrica y permitir la comunicación de las señales de los sensores con el programa.

### 7. Conexiones eléctricas

Para los sensores infrarrojos de barrera con salida digital se utilizaron las siguientes conexiones:

| IR #1 | Arduino | IR #2 | Arduino |
|------|---------|------|---------|
| VCC | 5V | VCC | 5V |
| GND | GND | GND | GND |
| OUT | Pin 2 (interrupción) | OUT | Pin 3 (interrupción) |

Los sensores se conectaron utilizando las entradas digitales correspondientes del Arduino.

*Nota:* La conexión del tercer sensor infrarrojo deberá agregarse de acuerdo con el pin que se utilizó en la práctica.

### 8. Conexión de la placa Arduino

Después de conectar los sensores a las protoboards, se conectaron los cables correspondientes desde la placa Arduino hacia las protoboards.

Se revisaron las conexiones eléctricas para comprobar que los sensores recibieran correctamente la alimentación y que sus señales llegaran a los pines establecidos.

### 9. Prueba de detección

Una vez realizadas las conexiones y cargado el programa, se comprobó que los sensores detectaran correctamente el paso de la pelota.

Se verificó que cada sensor generara la señal correspondiente cuando la pelota interrumpía la barrera infrarroja.

### 10. Realización de las mediciones

Se colocó la pelota pequeña en el inicio de la canaleta y se dejó avanzar.

Al pasar frente al primer sensor, se registró el primer tiempo.

Posteriormente, la pelota pasó frente al segundo sensor y se registró el segundo tiempo.

Finalmente, al pasar frente al tercer sensor, se registró el tercer tiempo.

### 11. Obtención de los tiempos

Con los tiempos registrados por los tres sensores fue posible obtener diferentes intervalos de tiempo:

- Tiempo entre el sensor 1 y el sensor 2.
- Tiempo entre el sensor 2 y el sensor 3.
- Tiempo entre el sensor 1 y el sensor 3.

### 12. Cálculo de la velocidad

Utilizando las distancias establecidas entre los sensores y los tiempos registrados, se calculó la velocidad correspondiente a cada tramo.

Para realizar los cálculos se utilizó:

*Velocidad = Distancia / Tiempo*

### 13. Repetición de las pruebas

Finalmente, se realizaron varias pruebas para comprobar el funcionamiento del sistema y comparar las mediciones obtenidas.

## Resultados

### Sensor 1 → Sensor 2

| Prueba | Distancia | Tiempo | Velocidad |
|--------|-----------|--------|-----------|
| 1 | [_] cm | [_] s | [_] cm/s |
| 2 | [_] cm | [_] s | [_] cm/s |
| 3 | [_] cm | [_] s | [_] cm/s |

### Sensor 2 → Sensor 3

| Prueba | Distancia | Tiempo | Velocidad |
|--------|-----------|--------|-----------|
| 1 | [_] cm | [_] s | [_] cm/s |
| 2 | [_] cm | [_] s | [_] cm/s |
| 3 | [_] cm | [_] s | [_] cm/s |

### Sensor 1 → Sensor 3

| Prueba | Distancia | Tiempo | Velocidad |
|--------|-----------|--------|-----------|
| 1 | [_] cm | [_] s | [_] cm/s |
| 2 | [_] cm | [_] s | [_] cm/s |
| 3 | [_] cm | [_] s | [_] cm/s |