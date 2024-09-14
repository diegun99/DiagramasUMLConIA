# DiagramasUMLConIA

conjunto de herramientas para generar diagramas UML con chatgpt

### Plant UML 

De código abierto, Usado para generar diagramas con una estructura sencilla
https://plantuml.com/

### Prompts de chatGPT a usar
#### Ejemplo:  

Genera código Plantuml para un diagrama de casos de uso de una tienda por departamentos

#### Resultado Generado

Dicho resultado se copia y se pega en plant UML para generar el diagrama; se pueden cambiar los colores y exportar en svg , jpg,etc

```
@startuml
left to right direction
skinparam packageStyle rectangle

actor "Cliente" as Cliente
actor "Empleado" as Empleado
actor "Gerente" as Gerente
actor "Proveedor" as Proveedor

package "Sistema de la Tienda por Departamentos" {
    usecase "Buscar Producto" as UC_BuscarProducto
    usecase "Añadir Producto al Carrito" as UC_AñadirCarrito
    usecase "Comprar Producto" as UC_ComprarProducto
    usecase "Consultar Historial de Compras" as UC_HistorialCompras
    usecase "Devolver Producto" as UC_DevolverProducto
    usecase "Gestionar Inventario" as UC_GestionarInventario
    usecase "Gestionar Pedidos a Proveedores" as UC_PedidosProveedores
    usecase "Generar Reportes de Ventas" as UC_ReportesVentas
}

Cliente --> UC_BuscarProducto
Cliente --> UC_AñadirCarrito
Cliente --> UC_ComprarProducto
Cliente --> UC_HistorialCompras
Cliente --> UC_DevolverProducto

Empleado --> UC_GestionarInventario
Empleado --> UC_DevolverProducto

Gerente --> UC_PedidosProveedores
Gerente --> UC_ReportesVentas

Proveedor --> UC_PedidosProveedores

@enduml

```
