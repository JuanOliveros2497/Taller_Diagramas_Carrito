**Juan Esteban Oliveros.**
**Daniel Stiven Poveda.**

## CODIGO WSD

``` plantuml
@startuml Diagrama de Timpo

robust "Usuario" as U
robust "Carrito" as S
robust "Pago" as DB
robust "Factura" as F

@0
U is "Registrarse" #white

@5
S is "Esperando solicitud" #white

@10
U -> S : Crear carrito
S is "Procesando consulta" #yellow

@15
S -> DB : Pagar Carrito
DB is "Hacer pago" #white

@20
DB -> S : Confirmar Pago
DB -> F : Crea Factura

@25
F is "Recibe detalle Factura" #white

@enduml


```
# Diagrama de  (Imagen)
![Diagrama de ](img/Sin%20título.png)

# DESCRIPCIÓN.

Un diagrama de tiempo (o diagrama de secuencia ) en formato WSD muestra la interacción entre diferentes objetos o componentes de un sistema en un orden temporal. En PlantUML, puedes crear diagramas de tiempo usando una estructura similar a la de los diagramas de secuencia.

Este diagrama de tiempo ilustra cómo fluyen las solicitudes y respuestas a lo largo del sistema en una secuencia cronológica.

# EXPLICACIÓN 

- USUARIO
  - El usuario se registra para poder acceder a la creacion de un carrito en el Tiempo (0).

- INICIAR SESION
  - Inicia sesión para acceser al carrito de compra y a los productos en el Tiempo (5) .

- CARRITO
  - Crea un IntemCarrito que almacena un conjunuto de productos en el Tiempo (10) .

- PAGO
  - Se genera al final del proceso de este carrito de compra, en el diagrama esta representado en el tiempo (20)

- FACTURA
  - Se genera despues de la acción de pago del carrito en el Tiempo (25) .

- DETALLE FACTURA
  - Se genera en consecuencia del pago dentro de la factura en el Tiempo (25) .