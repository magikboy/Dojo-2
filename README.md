

# Trabajo Practico N°2
Sistema de Procesamiento de Datos (SPD)
Ejercicio Estacion de subte

![Tinkercad](/assets/img/ArduinoTinkercad.jpg)


## Integrantes

* [Bosco Mascaro Massimo Ariel](https://github.com/magikboy)
* [Garcia Dottori Martin](#)
* [Gargiulo Mundo Camila](#)
* [Hruszczak Nicolas Gabriel](https://github.com/Nicolasgh91)
* [Hermosilla Sebastián Emanuel](https://github.com/EM40a)


## Proyecto: Semáforos para no videntes.

![Semáforos para no videntes](/assets/img/Sem%C3%A1foros%20para%20no%20videntes.png)

## Descripción

El gobierno de la cuidad quiere actualizar los semáforos que tienen instalados. Por lo cual estos mismos tienen que tener señalización para personas no videntes
nuestra solucion al problema es implementar una serie de bocinas sonaran durante el funcionamiento del semaforo.

Cuando se pare en la luz roja emitira un sonido continuo adviertiendole al peaton detenerse y no cruzar. En el cambio de semaforo, en la luz amarilla, emitira un sonido discontinuo avisando sobre el cambio de luz hacia el verde.


## Función principal

``` C++
void PrenderSemaforo(int luz, int tiempo, int frecuencia, int entretiempo)
{
  for (int i = 0 ; i < tiempo; i++) 
  {
    SonarBuzzer(luz, frecuencia, entretiempo);
    digitalWrite(luz, LOW);
  } 
}
```

### Explicacion

Enciende y apaga el buzzer junto al led correspondiente durante el tiempo indicado.

Recibe como parametros:

+ **luz** (el led/pin), de tipo entenro, que va a encender junto a la buzzer.
+ **tiempo** que durará la luz encendida. Dentro del for, lo que hace es ir iterando llamando a la funcion `SonarBuzzer` que enciende el led y la bocina a la vez.
+ **frecuencia** es el segundo parametro que recibe la funcion **tone** dentro de `SonarBuzzer` que es la frecuencia del tono en Hz.
+ **entreTiempo** es el tiempo entre cada sonido del buzzer en milisegundos.

---
## <img src="assets/img/tinkercad-logo.png" alt="Tinkercad" height="32px"> Link al proyecto

- [Proyecto](https://www.tinkercad.com/things/0eFa38BwfAQ-super-migelo-jofo/editel?sharecode=rXB4PgoPveKdescEf7ZKr18V5jzex0wzRh-1nmglAt4)

### Trabajo Practico:

[Consignas](https://github.com/magikboy/Dojo-N-mero-Uno/blob/18c1342eff3a6e0bedfadace646459866021de35/Dojo%20Numero%20Uno.pdf)

### Fuentes

- [Chat-GPT](https://chat.openai.com/)
- Youtube
- [Vladimir Guajardo Gonzalez](https://www.youtube.com/@SethPonder5/videos)
