# Descripción del proyecto
En este proyecto se realizo el codigo para que con la placa stm32l053 
se pueda detectar y visualizar una tecla pulsada en un teclado matricial
de 4x4, tambien se requiere que cuando se presione la tecla numeral, se limpie 
el diplay de 7 segmentos, es decir este en blanco y que cuando se presione
la tecla el coton de asterisco se visualice un boton previamente apachado 
es decir el anterior a este, para lo cual se exoplica a continuacion el codigo.

La estragia consiste en crear dos funciones en este caso:
ky_files() y ky_col() dichas funciones contienen la forma en que se va recorrer 
las filas y columnas del keypad, en este caso las filas seran puestas en pull up 
que quiere decir que estas cerraran el circuito para poder detectar la tecla que 
lleva el voltaje a cero, por otra parte en la funcion de columnas limpiara primero 
y cuando detecte la entrada junto con el boton correspondiente, este tiene la condicion
que se convierta en un caso, cada caso es guardado en una variable temporal, la cual se
se usara en la maquina de estados un switch case para que cuando se de determinado estado
se encienda los led correspondientes en el display 
Para limpiar el diplay unicamente hacemos el caso y poniendo en 0xFF y en este caso ningun led se encendera.
Dentro de las condicionales tenemos una variable en la que se guarda el valor anterior
es decir un ciclo antes que se presione el asterisco, de esta manera cuando este sea presionado 
se tiene la condición de que mande a llamar dicha variable que tiene almacenado el valor de un ciclo anterior y de esta manera mostrara el ultimo boton apachado

para su demostracion en este enlace se puede observar un video con su funcionamiento
[
](https://www.youtube.com/watch?v=vxPfNEILpgk)
