## Sistema de procesamiento de datos 
![Tinkercad](https://github.com/RocioIzaguirre/Parcial_SPD_parte1/blob/main/spd/primer%20parcial%20spd.png)

## Integrantes 
- Alonso Tomas
- Izaguirre Rocio 


### :computer: PRIMERA PARTE

# Proyecto: Contador de 0 a 99 
![Tinkercad](https://github.com/RocioIzaguirre/Parcial_SPD_parte1/blob/main/spd/Parte_1/Imagenes/Arduino_p1.png)


# :page_with_curl: Descripción
Hicimos un contador de 0 a 99 utilizando dos displays de 7 segmentos y tres botones para
controlar la cuenta. Implementamos la técnica de multiplexación para mostrar los dígitos
en los displays. El contador comienza en 0 y es capaz de aumentar o disminuir
su valor en una unidad con los botones.

# Función principal

mostrarContador(int contador) recibe el contador del segun el boton presionado en el caso de la decena 

~~~ C (lenguaje en el que esta escrito)
void mostrarContador(int contador){
	
	prenderSegmento(APAGADO);
	mostrarNumero(contador/10);
    	prenderSegmento(DECENA);
    	prenderSegmento(APAGADO);
    	mostrarNumero(contador - 10*((int)contador/10));
  	prenderSegmento(UNIDAD);
}
~~~

#  :bulb: Link al proyecto
- [proyecto](https://www.tinkercad.com/things/4lFIXDyPHY5-parcialp1/editel?sharecode=VXzAnD9cqqI3S3z6hozVn4Gwyo1SRIBewK1CanuHU-w)




### :computer: SEGUNDA PARTE
# Proyecto: Contador de 0 a 99. -> Modificación: Interruptor Deslizante, Números Primos, Motor y Sensor de temperatura.
![Tinkercad](https://github.com/RocioIzaguirre/Parcial_SPD_parte1/blob/main/spd/Parte_2/Imagenes/Arduino_p2.png)

# :page_with_curl: Descripción

Modificamos la parte 1 quitando un boton y agregando un interruptor deslizante (switch) de dos posiciones.
Dependiendo de la posición del interruptor, el display mostrara o bien el contador (como
en la Parte 1) o los números primos en el rango de 0 a 99.
El motor se enciende dependiendo de la temperatura. Se encendera si la temperatura sale de un determinado rango. 


# Función agregada

Funciones encontrar proximo o anterior numero primo. 


~~~ C (lenguaje en el que esta escrito)
int encontrarProximoPrimo(int numeroInicial) {
  int numero = numeroInicial;
  while (true) {
    if (esPrimo(numero) == 1)
      return numero;
    numero++;
  }
}
int encontrarPrimoAnterior(int numeroInicial) {
  int numero = numeroInicial;
  while (true) {
    if (esPrimo(numero) == 1)
      return numero;
    numero--;
  }
~~~

#  :bulb: Link al proyecto
- [proyecto](https://www.tinkercad.com/things/iTWAIc2E8oB-parcialp2/editel?sharecode=w0u_H0nxvnT8rUE2MMIlaW9kSQX-LEVkb5tj0LduRa8)

### :computer: TERCERA PARTE
# Proyecto: Fotorresistencia.
![Tinkercad](https://github.com/RocioIzaguirre/Parcial_SPD_parte1/blob/main/spd/Parte_3/Imagenes/Arduino_p3.png)

# :page_with_curl: Descripción

Modificamos la parte 1 y 2 agregando una fotorresistencia, esta encendera una luz (led) cada vez que la luz baje.

# Función agregada

La luz se encendera

~~~ C (lenguaje en el que esta escrito)
  lecturaFotorresistencia = analogRead(LECTURA_FOTORRESISTENCIA);
  fotorresistencia = map(lecturaFotorresistencia,348,1017,1,10);
  Serial.println(fotorresistencia);
  if(fotorresistencia>7){
  digitalWrite(LED_AMARILLO,HIGH);
  }
  else{
  digitalWrite(LED_AMARILLO,LOW);
  }
~~~

#  :bulb: Link al proyecto
- [proyecto](https://www.tinkercad.com/things/aPytYa3sQz8-parcialp3/editel?sharecode=mWizTtkcN0jhysMXRFka33HydxYDKEHA5D0L-soYiSs)

- ### :computer: CUARTA PARTE

# Proyecto: Utilizar el interruptor deslizante para encender y apagar todo el sistema.
![Tinkercad](https://github.com/RocioIzaguirre/SPD_Primer.parcial/blob/main/spd/Parte_4/Imagenes/Arduino_4.png)


# :page_with_curl: Descripción
Modificamos la parte 1 , 2 y 3. El interruptor ahora encedera y apagara todo el sistema dependiendo de su posicion. 

# Función principal

El interruptor cuando se encuentra en LOW apaga todo el sistema. 

~~~ C (lenguaje en el que esta escrito)
else if (interuptor == LOW){
        digitalWrite(LED_A, APAGADO);
        digitalWrite(LED_B, APAGADO);
	digitalWrite(LED_C, APAGADO);
  	digitalWrite(LED_D, APAGADO);
  	digitalWrite(LED_E, APAGADO);
  	digitalWrite(LED_F, APAGADO);
  	digitalWrite(LED_G, APAGADO);
        digitalWrite(MOTOR, APAGADO);
        digitalWrite(LED_AMARILLO, APAGADO);
  
  }
}
~~~

#  :bulb: Link al proyecto
- [proyecto](https://www.tinkercad.com/things/iasq3kgDCPr-parcialp4/editel?sharecode=h3-37Z46YOkpQFF8SFN_ECWYaMKvT3xVvPhWZTnwnjY)


