# Create Product with Upnify

Creates a new product in Upnify.

## Endpoint

- **Method:** `POST`
- **Path:** `v4/catalogos/productos`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Create Product](https://desarrollo.upnify.com/api-rest/catalogos/#api-Productos-PostCatalogosProductos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idProductoServicioMx` | body | `number` | yes | Identificador que define el código del catálogo de productos del SAT utilizado.  ¿Dónde obtengo el id? |
| `idUnidadMx` | body | `number` | yes | Identificador que define el código del catálogo de unidades del SAT.  ¿Dónde obtengo el id? |
| `codigo` | body | `string` | yes | Contiene un código que puede ser establecido por el usuario para poder identificar el producto en el sistema. |
| `nombre` | body | `string` | yes | Guarda el nombre con el que el producto que se registró en el sistema. |
| `costo` | body | `number` | yes | Guarda el costo real del producto. |
| `unidad` | body | `string` | yes | Muestra la unidad de medida utilizada para contabilizar el producto. |
| `precioMinimo` | body | `number` | yes | Contiene el costo de venta al público del producto este precio no puede ser menor al costo real del producto. |
| `existencia` | body | `number` | yes | Guarda la cantidad de productos disponibles. |
| `tkMarca` | body | `string` | yes | Código que corresponde e identifica de forma única a una marca.  ¿Dónde obtengo el token? |
| `tkLinea` | body | `string` | yes | Código que corresponde e identifica de forma única a una línea de productos.  ¿Dónde obtengo el token? |
| `precio1` | body | `number` | yes | Establece el monto a asignar para la primera lista de precio configurada en el sistema. Se pueden colocar hasta 10 parámetros de precio, ("precio1","precio2","precio3", ...), uno por cada lista de precio configurada en el sistema. Para determinar que lista de precio corresponde a cada parámetro "PRECIO", es necesario obtener el "indiceLista" de las listas de precio.  ¿Dónde obtengo el indice de la lista de precio? El monto de mi lista de precio con "indiceLista": "1" , se debe enviar en el parámetro "precio1". El monto de mi lista de precio con "indiceLista": "2" , se debe enviar en el parámetro "precio2". Así sucesivamente. |
| `comision1` | body | `number` | yes | Establece el monto a asignar para la primera comisión del producto. Se pueden colocar hasta 10 parámetros de comision, ("comision1","comision2","comision3", ...), uno por cada comisión configurada en el sistema. Para determinar que comisión corresponde a cada parámetro "comision", es necesario obtener el "indiceComision" de las comisiones configuradas.  ¿Dónde obtengo el indice de las comisiones? El monto de mi comision con "indiceComision": "1" , se debe enviar en el parámetro "comision1". El monto de mi comision con "indiceComision": "2" , se debe enviar en el parámetro "comision2". Así sucesivamente. |
| `impuesto1` | body | `number` | yes | Establece el monto del primer impuesto trasladado configurado en el sistema. Se pueden colocar hasta 10 parámetros de impuesto, ("impuesto1","impuesto2","impuesto3", ...), uno por cada impuesto configurado en el sistema. Para determinar impuesto corresponde a cada parámetro "impuesto", es necesario obtener el "indiceImpuesto" de los impuestos configurados.  ¿Dónde obtengo el indice de los impuestos? El monto de mi impuesto con "indiceImpuesto": "1" , se debe enviar en el parámetro "impuesto1". El monto de mi impuesto con "indiceImpuesto": "2" , se debe enviar en el parámetro "impuesto2". Así sucesivamente. |
| `impuestoR1` | body | `number` | yes | Establece el monto del primer impuesto retenido configurado en el sistema. Se pueden colocar hasta 10 parámetros de impuestoR, ("impuestoR1","impuestoR2","impuestoR3", ...), uno por cada impuesto configurado en el sistema. Para determinar impuesto corresponde a cada parámetro "impuesto", es necesario obtener el "indiceImpuesto" de los impuestos configurados.  ¿Dónde obtengo el indice de los impuestos? El monto de mi impuesto con "indiceImpuesto": "1" , se debe enviar en el parámetro "impuestoR1". El monto de mi impuesto con "indiceImpuesto": "2" , se debe enviar en el parámetro "impuestoR2". Así sucesivamente. |
