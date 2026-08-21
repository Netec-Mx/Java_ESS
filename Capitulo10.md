## Introducción ##

> Para reforzar la teoría vista hasta el momento durante el curso, realizaremos una serie de ejercicios que buscan que utilicemos los conocimientos aprendidos sobre Interfaces, el API de fechas de Java y Excepciones.

## Objetivos ##

> Repasar Funcionalidades de Java como lo son las Excepciones, el API de Fechas y el manejo de las interfaces / clases abstractas.

### Planteamiento inicial: ###

> Continuando sobre el proyecto del ejercicio anterior, continuaremos desarrollando nuevas funcionalidades sobre el mismo proyecto de banca electronica.

### Tareas ###

1. En el mismo proyecto BancaElectronica, en el paquete modelo crea la clase Banco y la interfaz ManejaClientes.

2. La interfaz ManejaClientes define los siguientes métodos:
* altaCliente(CuentaHabiente):void
* bajaCliente(numero):void
* consultaCliente(numero):CuentaHabiente
* actualizaCliente(domicilio):void

3. La clase banco cuenta con los siguientes atributos encapsulados:

* nombre(String)
* domicilio (String)
* telefono(String)
* clientes (ArrayList<CuentaHabiente>)

y los siguientes métodos:

* Banco(nombre, domicilio, telefono)
* imprimirClientes()
* toString()

![UML1](./imagenes/Imagen-12-01.png)

4. Implementa la interface ManejaClientes.

5. Cambia el tipo de variable “clientes” al tipo interface List, vuelve a compilar el proyecto y verifica si hay que realizar algún cambio en la programación.

6. Modifica la clase Cuenta que se definió en el Laboratorio pasado, agrega un nuevo atributo tipo LocalDate califícalo como protected y llámalo fechaAlta, agrega los métodos set/get para este nuevo atributo.

7. Modifica el constructor para que se inicialice el atributo fechaAlta en tiempo de creación de la cuenta.

8. Modifica el método imprimirCuenta para que se vea reflejado este atributo.

9. Agrega un nuevo método llamado calculaVigencia, que imprima cuánto tiempo lleva la cuenta activa desde que fue creada, prueba este método cambiando la fecha de alta con el método set.

10. Realiza el cambio necesario en el método retiro en la cuenta de inversión para que solo deje hacer retiros una vez terminado el periodo de 6 meses usando el método calculaVigencia.

11. Prueba estos cambios comprobando que funcionan de manera adecuada.

12. Crea una nueva excepción, nómbrala “SaldoInsuficienteException.” Modifica el método retiro de la clase CuentaAhorros para que, cuando no haya saldo suficiente en la cuenta, lance la excepción con la sentencia throw para indicar que no hay suficiente saldo en la cuenta para hacer el retiro.

13. Crea otra nueva excepción, nómbrala “OperacionInvalidaException.” Modifica el método retiro de la clase CuentaInversion para que, cuando no haya pasado el tiempo obligatorio de 6 meses, lance la excepción para indicar que aún no se pueden realizar retiros.

![UML2](./imagenes/Imagen-12-02.png)

14. Usa la cláusula throws para dejar salir de cada método la excepción. 

15. En la clase donde tenemos el main, escribe el código necesario para probar que las excepciones creadas en el laboratorio anterior funcionan de manera correcta. 