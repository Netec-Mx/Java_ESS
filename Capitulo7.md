## Introducción ##

> Para reforzar la teoría vista hasta el momento durante el curso, realizaremos una serie de ejercicios que buscan que utilicemos los conocimientos aprendidos sobre programación orientada a objetos

## Objetivos ##

> Repasar conceptos de Programación Orientada a Objetos, como por ejemplo sobre carga, sobre escritura, encapsulamiento, y en general el comportamiento de Java.

### Planteamiento inicial: ###

> Para esta serie de ejercicios se utilizará un nuevo proyecto donde se desarrollaran una serie de tareas y funciones que buscan integrar varios conceptos cubiertos en el curso dentro de un escenario que simula el comportamiento de un banco.

## Tareas ##

1. Crea un nuevo proyecto y llámalo BancaElectronica.

2. Define un paquete llamado modelo y en él una clase llamada Cuenta que represente a una cuenta bancaria. Sobre el mismo paquete, define otra clase llamada PruebaCuenta.

3. Dentro de Cuenta agrega los atributos:     
* numeroCuenta(int)
* tipoCuenta(char)
* saldo(double).

4. Define un constructor que reciba todos los datos de la cuenta, así como los métodos mínimos que den funcionalidad, como son:
* void deposito(double)
* double retiro(double). 
* imprimirCuenta que imprima todos los datos de la cuenta.


5. Coloca el método main en la clase PruebaCuenta, crea dentro del main una cuenta realizando algunos movimientos, posteriormente imprime los datos de la cuenta incluyendo el saldo final.

![UML1](./imagenes/Imagen-07-01.png)

6. Define una nueva clase llamada CuentaHabiente en el paquete modelo con los atributos nombre, domicilio, teléfono y un atributo cuentas de tipo ArrayList<Cuenta>.

7. Sobre la clase CuentaHabiente, escribe e implementa los siguientes métodos: 
* Constructor (que reciba todos los datos del cuenta habiente e inicialice el ArrayList), 
* agregarCuenta(Cuenta), 
* consultarCuenta(numero), 
* eliminarCuenta(numero)
* listarCuentas(). 

![UML2](./imagenes/Imagen-07-02.png)

8. Sobre la clase PruebaCuenta, crea un objeto CuentaHabiente y una o más cuentas para el mismo cuenta habiente. Prueba cada uno de los métodos definidos en CuentaHabiente.

9. Modifica la clase Cuenta creada anteriormente encapsulando todos los atributos marcándolos como privados y definiendo sus respectivos métodos públicos (los que ya existían más los métodos set y get por cada uno).

![UML3](./imagenes/Imagen-07-03.png)

10. Modifica el método retiro, deberás validar que la cantidad retirada no exceda el saldo, en caso contrario deberás imprimir la leyenda “saldo insuficiente”.

11. Modifica los métodos retiro y deposito para que por cada operación que se realice se deberá reportar el tipo de operación y el saldo de la cuenta resultante, por ejemplo: 
    Cuenta: 120345, Operación: retiro 100 pesos, saldo 900
    Cuenta: 120345, Operación: abono 200 pesos, saldo 1100

12. En la clase PruebaCuenta, verifica que los cambios funcionan correctamente.

13. Modifica la clase CuentaHabiente para que el método agregarCuenta(Cuenta) no agregue una cuenta repetida y haz que en el método eliminarCuenta(numero) mande llamar dentro de si al método buscarCuenta y dependiendo del resultado se elimine la cuenta de la lista de cuentas.

14. En la clase PruebaCliente, verifica que todos los cambios funcionan como se espera.

15. Define dos subclases llamadas CuentaInversión y CuentaCheques que hereden de la clase Cuenta.

16. Cambia el modificador de acceso de cada atributo en la clase Cuenta de private a protected para que los atributos sean accesibles de manera directa a sus subclases.

17. En la CuentaCheques, define una nueva variable de instancia que se llame protección (double).

18. La protección anterior le permitirá al cuenta habiente exceder su saldo al emitir un cheque hasta por el monto de esa protección de sobregiro, por lo que deberás sobre escribir el comportamiento del método retiro para permitir operaciones hasta por el monto de la protección sin ninguna penalización adicional, en caso de un sobregiro mayor a dicha protección, deberá rechazar la operación y penalizará a la cuenta con el 10% del monto del cheque rechazado. Para ambos casos el método debe informar al usuario que esta haciendo una operación por sobre el valor que tiene disponible.

19. Sobre escribe el método imprimirCuenta() para poder ver los datos de la cuenta de cheques.

20. Las siguientes acciones se deberán llevar acabo sobre la Clase CuentaInversión.- las cuentas de inversión siempre se abren a un periodo fijo de 6 meses con una tasa de interés fija en el periodo, no se puede disponer del dinero durante ese periodo y tampoco se puede aumentar el saldo de la cuenta. 
* Define un constructor para la cuenta de inversión que será creada con los siguientes datos: número de cuenta, tipo, saldo inicial y tasa de interés semestral(double). 
* El atributo tasaInteresSemestral deberá ser una constante en tiempo de creación de la cuenta. 
* Sobre escribe el método imprimirCuenta para imprimir los datos de la cuenta de inversión con los intereses a ganar en el periodo. 
* Para proteger la cuenta de inversión para que no se realicen depósitos o retiros durante el periodo de 6 meses, tendremos que agregar un nuevo campo, fecha de apertura (String), dicho campo de momento no haremos todavía nada con el, pero en siguientes capítulos lo modificaremos para usarlo en los métodos retiro y deposito sobre escritos.

![UML4](./imagenes/Imagen-07-04.png)


21. Define en la clase PruebaCuenta una cuenta de inversión y de cheques, aplícales los métodos definidos y comprueba que se comportan de la manera esperada.

22. Marca la clase Cuenta como abstracta. Intenta crear una instancia de la clase Cuenta, ¿qué es lo que observas? ¿Tiene sentido crear objetos de la clase Cuenta?

23. Define un nuevo método en la clase Cuenta con la siguiente definición: public abstract String descripcionDeLaCuenta(); 

Cuando compiles el código, ¿qué sucederá con las subclases?

24. Implementa el método descripcionDeLaCuenta() en cada subclase para que despliegue un mensaje adecuado al tipo de cada cuenta, prueba los métodos.