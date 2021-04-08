# PRÀCTICA 1 
## CÓDIGO
```
#include <Arduino.h>
/*
  Blink
  Turns on an LED on for one second, then off for one second, repeatedly.
 
  This example code is in the public domain.
 */
 
// Pin 13 has an LED connected on most Arduino boards.
// give it a name:
int led = 13;

// the setup routine runs once when you press reset:
void setup() {  
  Serial.begin(115200);              
  // initialize the digital pin as an output.
  pinMode(led, OUTPUT);     
}

// the loop routine runs over and over again forever:
void loop() {
  digitalWrite(led, HIGH);   // turn the LED on (HIGH is the voltage level)
  Serial.println("on");
  delay(500); 
  digitalWrite(led, LOW);    // turn the LED off by making the voltage LOW
  Serial.println("off");              // wait for a second
   delay(500);               // wait for a second
}
```
## DIAGRAMA DE FLUJO
``` mermaid
graph TD 
    A(Turn the LED on)-->B(print on);
    B-->C(wait for 500 ms);
    C-->D(turn the LED off);
    D-->E(print off);
    E-->F(wait for 500 ms);
    F-->A;
```

## DIAGRAMA DE TIEMPOS
```wavedrom
{ signal: [
  { name: "LED",    wave: "101010101" },
  { name: "time",   wave: "343434343", data: ["0.5s", "0.5s", "0.5s", "0.5s", "0.5s", "0.5s", "0.5s", "0.5s", "0.5s"] }
]}

```