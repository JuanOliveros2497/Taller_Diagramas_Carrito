**Juan Esteban Oliveros.**
**Daniel Stiven Poveda.**

## CODIGO WSD

``` plantuml
@startuml  DiagramaDeEstado 

[*] --> USUARIO
USUARIO --> REGISTRO: Registro del usuario
REGISTRO-right-> PRODUCTO: Acceso a los porductos
PRODUCTO-down-> CARRITO:  Agrego productos
CARRITO -left-> ITEMCARRITO: Creo un conjunto de productos
ITEMCARRITO --> PAGO: Pago el carrito de productos
PAGO -right-> FACTURA:Recibo factura 
FACTURA--> DETALLEFACTURA: Recibo detelles de la factura
DETALLEFACTURA --> [*]


REGISTRO : Procesos de registro de Usaurio 
PRODUCTO : Vista y accesto a los Productos
CARRITO : Creaccion de un Nuevo carrito
ITEMCARRITO : Conjunto de productos agragado al carrito
PAGO: Pago del Carrito 
FACTURA: Factura de pago
DETALLEFACTURA: Detalles de la factura de Pago

@enduml

```
# Diagrama de Estado (Imagen)
![Diagrama de estado](img/Diagrama-de-Estado.png)

# DESCRIPCIÓN.

Así es, el Diagrama de Estados, también conocido como Diagrama de Estado-Transición o Diagrama de Máquina de Estados, es una representación gráfica de los posibles estados que puede tener un objeto y las transiciones que ocurren entre estos estados como respuesta a eventos específicos. Este tipo de diagrama se usa en el modelado de sistemas para comprender cómo los objetos cambian de estado en función de las interacciones o condiciones externas, y es especialmente útil en el diseño de software orientado a objetos.


# EXPLICACIÓN 

- USUARIO
  - El usuario se registra para poder acceder a la vista de productos y a la creación de un carrito.

- INICIAR SESION
  - Inicia sesión para acceser al carrito de compra y a los productos.

- CARRITO
  - Crea un IntemCarrito que almacena un conjunuto de productos.

- PRODUCTO
  - Esta incormporado para que el usuario tenga una vista de los producos que ingrasa al carrito y quedan gaurdados en ItemCarrito.

- PAGO
  - Se genera al final del proceso de este carrito de compra

- FACTURA
  - Se genera despues de la acción de pago del carrito.

- DETALLE FACTURA
  - Se genera en consecuencia del pago dentro de la factura.