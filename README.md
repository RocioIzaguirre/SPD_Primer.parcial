## Sistema de procesamiento de datos 
![Tinkercad](https://github.com/RocioIzaguirre/Parcial_SPD_parte1/blob/main/spd/primer%20parcial%20spd.png)

## Integrantes 
- Acevedo Facundo 
- Alonso Tomas
- Izaguirre Rocio 


### :computer: PRIMERA PARTE

# Proyecto: Contador de 0 a 99 
![Tinkercad](https://github.com/RocioIzaguirre/Parcial_SPD_parte1/blob/main/spd/Parte_1/Imagenes/Arduino_p1.png)


# Descripción
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

# Descripción

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
# Proyecto: Agregar una fotorresistencia.
![Tinkercad](https://github.com/RocioIzaguirre/Parcial_SPD_parte1/blob/main/spd/Parte_3/Imagenes/Arduino_p3.png)

# Descripción

Modificamos la parte 1 y 2 agregando una fotorresistencia, esta se encendera cada vez que la luz baje.

# Función agregada

Funciones encontrar proximo o anterior numero primo. 


~~~ C (lenguaje en el que esta escrito)

~~~

#  :bulb: Link al proyecto
- [proyecto](https://www.tinkercad.com/things/aPytYa3sQz8-parcialp3/editel?sharecode=mWizTtkcN0jhysMXRFka33HydxYDKEHA5D0L-soYiSs)


