## Parcial domiciliario de la materia SPD

## Integrantes 
- Tomás Alonso
- Rocio Izaguirre
- Facundo Acevedo

### PRIMERA PARTE
# Proyecto: Contador de 0 a 99 con Display 7 Segmentos y Multiplexación.
![Tinkercad]()
![Tinkercad](https://github.com/TomiAlo/parcial_domicialiario_spd/blob/main/Parcial%20domilicario%20SPD/primera%20parte/img/arduino.png)


# Descripción
Un contador de 0 a 99 utilizando dos displays de 7 segmentos y tres botones para
controlar la cuenta. Implementando la técnica de multiplexación para mostrar los dígitos
en los displays. El contador debe comenzar en 0 y debe ser capaz de aumentar o disminuir
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

# :robot: Link al proyecto
- [proyecto](https://www.tinkercad.com/things/7bqVfm3cuZj-tomas-alonso-parcial-domiciliario-primera-parte/editel?sharecode=RHi6H5vBMP38nDHCA2IBRw17-K7im3VYH2voxiM1qeE)




### SEGUNDA PARTE
# Proyecto: Contador de 0 a 99 con Display 7 Segmentos y Multiplexación -> Modificación con Interruptor Deslizante, Números Primos, Motor y Sensor de temperatura.
![Tinkercad](https://github.com/TomiAlo/parcial_domicialiario_spd/blob/main/Parcial%20domilicario%20SPD/segunda%20parte/img/arduino.png)


# Descripción

Modifica el proyecto de la Parte 1 de la siguiente manera:
Sustituye uno de los botones por un interruptor deslizante (switch) de dos posiciones.
Dependiendo de la posición del interruptor, el display debe mostrar o bien el contador (como
en la Parte 1) o los números primos en el rango de 0 a 99.
Despues agregar un sensor de temperatura y un motor de aficionado.


# Función agregada

Funcion esPrimo recibe un numero y retorna un 1 en caso de ser primo 


~~~ C (lenguaje en el que esta escrito)
int esPrimo(int numero) {
  int cont_primo=0;
  for(int i=1;i<=numero;i++)//divide a el numero por todos los numero anteriores a si mismo hasta llegar
  {                         //a dividirse por si mismo 
  	if (numero%i==0)        //Si el resto de alguna de esas divisiones es 0 lo sumo a mi contador
    	cont_primo ++;
  }
  	if(cont_primo==2)  //Si mi contador es igual a dos es primo porque los numeros primos son divisibles
    	return 1;     //solo por 1 y por si mismo.
    else
 		return 0;
}
~~~

# :robot: Link al proyecto
- [proyecto](https://www.tinkercad.com/things/kuIwrJLp3Ca-copy-of-tomas-alonso-parcial-domiciliario-primera-parte/editel?sharecode=ewSI4DiXY7VyP3ky_9xckHDwe7PtIVlhlXu0descZQc)


