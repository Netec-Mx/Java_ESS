## Introducción ##

> Para reforzar la teoría vista hasta el momento durante el curso, realizaremos una serie de ejercicios que buscan que utilicemos los conocimientos aprendidos sobre arreglos y ciclos para poder resolver una serie de problemas.


## Objetivos ##

> Reforzar la funcionalidad de los bucles y arreglos.

### Planteamiento inicial: ###

> Sobre el mismo programa principal, agregaremos los siguientes programas en el mismo menu para poder acceder a la nueva funcionalidad.

![Menu](./imagenes/Imagen-03-00.png)

### Ejercicios fáciles: ###

1) Dias de vacaciones

Con base a la siguiente imagen

![Vacaciones](./imagenes/Imagen-04-01.png)

Escribe un programa en Java que utilice un arreglo que defina el número de días que se le pagará a un empleado, dado el número de años trabajados.

Siendo la posición del arreglo el numero de años que ha trabajado la persona.

De esta manera cuando el usuario ingrese su antigüedad le devuelva la cantidad de vacaciones que tiene disponible.

![Vacaciones](./imagenes/Imagen-04-02.png)

2) Pruebas ArrayList
Crea un programa que haga uso de la clase ArrayList para almacenar las siguientes cadenas: uno, dos, tres, cuatro, cinco.

Imprime los valores con un ciclo for each.

Inserta al inicio del ArrayList la cadena cero.

Elimina las cadenas dos y cuatro

Imprime de nuevo los elementos resultantes y el tamaño resultante del arreglo.

3) Números primos 

Escribe un programa en Java que utilice un ciclo for indexado que imprima los primeros 20 números primos.

Los números primos son aquellos números naturales mayores a 1 que solamente se pueden dividir por sí mismos, es decir, si los dividimos por cualquier otro número, el resultado no es entero.

![Primos](./imagenes/Imagen-04-03.jpg)

4) Factorial 

Escribe un programa en Java que utilice un do-while para calcular el factorial de un número entre 1 y 10.

El factorial de un número es la multiplicación de los números que van del 1 a dicho número. Para expresar el factorial se suele utilizar la notación n!. Así la definición es la siguiente: n! =1 x 2 x 3 x 4 x 5 x ... x (n-1)x n 

![Factorial](./imagenes/Imagen-04-04.jpg)



### Ejercicios Intermedios: ###


1) Estacionamiento

Define un arreglo de tamaño tres, siendo cada uno de estos espacios un  tipo de espacio de estacionamiento. 

Los tipos de estacionamientos son: grande (vehículos con dimensiones muy grandes), mediano (la mayoría de vehículos) y motocicletas, para cada tamaño hay un número fijo de espacios.

![Estacionamiento](./imagenes/Imagen-04-07.png)

Se le debe solicitar al usuario la cantidad de aparcamientos que tendrá el estacionamiento para cada tipo de vehículo.

Posteriormente el programa debe entrar en un bucle para ir ingresando algún tipo de vehículo e ir actualizando la cantidad de espacios disponibles.

Los vehículos solo pueden estacionar en un cajon que sea de su tipo correspondiente.
En caso de que 
no exista un espacio disponible, debe indicarle al usuario que no puede estacionar y terminar el programa.


2) Palíndromo

Un palíndromo es una palabra o frase que se lee igual hacia adelante y hacia atrás (ignorando espacios, puntuación y mayúsculas).

![Palíndromo](./imagenes/Imagen-04-05.png)

Por ejemplo, "anilina" es un palíndromo.

Por lo que se debe elaborar un programa que le solicite al usuario una cadena de texto y el programa debe validar que efectivamente sea un palíndromo.


3) Anagrama

Un anagrama es una palabra o frase formada al reordenar las letras de otra palabra o frase,
generalmente utilizando todas las letras originales exactamente una vez.

![Palíndromo](./imagenes/Imagen-04-06.jpg)

Por lo que considerando lo anterior, elabora un programa que valide si dos palabras pueden ser un anagrama entre si.

4) Compra - Venta en bolsa

El programa tiene dos diccionarios, uno con los precios de compra de una acción en distintos días y otro con los precios de venta de la misma acción en distintos días. 

El programa debe determinar cual es la combinación de los mejores días para comprar y vender la acción para maximizar la ganancia, es decir, comprar a un precio 
bajo y vender a un precio alto. La principal restricción es que el dia de compra  debe ser anterior al dia de venta
Ejemplo: 
compra = [7, 1, 5, 3, 6, 4, 5], 
venta = [10, 5, 3, 6, 4, 8, 3] -> 
comprar el dia 2 (precio 1) y vender el dia 6 (precio 8) para obtener una 
ganancia de 7

![Acciones](./imagenes/Imagen-04-08.png)