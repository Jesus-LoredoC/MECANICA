# CÓDIGOS UTILIZADOS

## PRÁCTICA 1

### Intermitencia

```cpp
// C++ code
//
/*
  This program blinks pin 13 of the Arduino (the
  built-in LED)
*/

void setup()
{
  pinMode(LED_BUILTIN, OUTPUT);
}

void loop()
{
  // turn the LED on (HIGH is the voltage level)
  digitalWrite(LED_BUILTIN, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  // turn the LED off by making the voltage LOW
  digitalWrite(LED_BUILTIN, LOW);
  delay(1000); // Wait for 1000 millisecond(s)
}
```

### Atenuación

```cpp
/*
  Fade

  This example shows how to fade an LED on pin 9 using the analogWrite() function.

  This example code is in the public domain.
*/

int led = 9;           // the PWM pin the LED is attached to
int brightness = 0;    // how bright the LED is
int fadeAmount = 5;    // how many points to fade the LED by

void setup() {
  // declare pin 9 to be an output:
  pinMode(led, OUTPUT);
}

void loop() {
  // set the brightness of pin 9:
  analogWrite(led, brightness);

  // change the brightness for next time through the loop:
  brightness = brightness + fadeAmount;

  // reverse the direction of the fading at the ends of the fade:
  if (brightness <= 0 || brightness >= 255) {
    fadeAmount = -fadeAmount;
  }
  // wait for 30 milliseconds to see the dimming effect
  delay(30);
}
```

### Botón

```cpp
Boton:
int buttonState = 0;

void setup()
{
  // Inicializa la comunicación serial a 9600 baudios
  Serial.begin(9600);
  
  pinMode(8, INPUT);
  pinMode(LED_BUILTIN, OUTPUT);
}

void loop()
{
  // Lee el estado del pulsador
  buttonState = digitalRead(8);
  
  // Muestra el valor en el Monitor Serie (0 o 1)
  Serial.println(buttonState);
  
  // Revisa si el pulsador está presionado
  if (buttonState == HIGH) {
    digitalWrite(LED_BUILTIN, HIGH);
  } else {
    digitalWrite(LED_BUILTIN, LOW);
  }
  
  delay(10); // Pausa corta para estabilidad
}
```

## Serie de lectura digital

```cpp
// C++ code
//
/*
  DigitalReadSerial

  Reads a digital input on pin 2, prints the
  result to the serial monitor

  This example code is in the public domain.
*/

int buttonState = 0;

void setup()
{
  pinMode(2, INPUT);
  Serial.begin(9600);
}

void loop()
{
  // read the input pin
  buttonState = digitalRead(2);
  
  // print out the state of the button
  Serial.println(buttonState);
  
  delay(10); // Delay a little bit to improve simulation performance
}
```

## Entrada Analógica

```cpp
int sensorValue = 0;

void setup()
{
  // Inicializa la comunicación serial a 9600 baudios
  Serial.begin(9600);
  
  pinMode(A0, INPUT);
  pinMode(LED_BUILTIN, OUTPUT);
}

void loop()
{
  // Lee el valor analógico del sensor
  sensorValue = analogRead(A0);
  
  // Muestra el valor leído en el Monitor Serie
  Serial.println(sensorValue);
  
  // Enciende el LED
  digitalWrite(LED_BUILTIN, HIGH);
  delay(sensorValue); // Espera el tiempo leído en milisegundos
  
  // Apaga el LED
  digitalWrite(LED_BUILTIN, LOW);
  delay(sensorValue); // Espera el tiempo leído en milisegundos
}
```

## Servomotor

```cpp
#include <Servo.h>

int pos = 0;

Servo servo_9;

void setup()
{
  // Inicializa la comunicación serial a 9600 baudios
  Serial.begin(9600);
  
  servo_9.attach(9, 500, 2500);
}

void loop()
{
  // Mueve el servo de 0 a 180 grados
  for (pos = 0; pos <= 180; pos += 1) {
    servo_9.write(pos);
    
    // Muestra la posición actual en el Monitor Serie
    Serial.println(pos);
    
    delay(15);
  }
  
  // Mueve el servo de 180 a 0 grados
  for (pos = 180; pos >= 0; pos -= 1) {
    servo_9.write(pos);
    
    // Muestra la posición actual en el Monitor Serie
    Serial.println(pos);
    
    delay(15);
  }
}
```