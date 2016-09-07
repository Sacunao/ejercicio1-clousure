# EJERCICIO CLOUSURE

Modificar el siguiente script usando closures para que se ejecute sin problemas.

var num2 = 0;

function suma(num1) {
	return function() {
		return num1 + num2;
	}
} 

var suma2 = suma(2);
console.log(suma2(5)); // Debería mostrar 7 de resultado

var suma12 = suma(12);
console.log(suma12(76)) // Debería mostrar 88 de resultado.

##RESOLUCIÓN:

Tal como está la función y la mandamos a inspeccionar encontramos la siguiente imagen:

![FLUJOGRAMA](http://2.1m.yt/nJdADev.jpg "Flujograma")


Donde se puede diferir:

1. El único valor que esta tomando la función es el 2 de num1.
2. La variable num2 no esta tomada como parametro en la función hija.
3. La variable global: var num2 = 0, no aporta nada porque lo único que haría es que se empiece de nuevo con un valor de cero.
5. Por lo tanto la resolución sería eliminar la varibale global y poner el parametro de num2 a la función hija de manera correspondiente.

