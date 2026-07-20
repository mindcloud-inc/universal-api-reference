# Upnify: Update Product

Updates an existing product in Upnify.

```
PUT https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idProductoServicioMx` | number | no | Identificador que define el código del catálogo de productos del SAT utilizado. ¿Dónde obtengo el id? |
| `idUnidadMx` | number | no | Identificador que define el código del catálogo de unidades del SAT. ¿Dónde obtengo el id? |
| `codigo` | string | no | Contiene un código que puede ser establecido por el usuario para poder identificar el producto en el sistema. |
| `nombre` | string | no | Guarda el nombre con el que el producto que se registró en el sistema. |
| `costo` | number | no | Guarda el costo real del producto. |
| `unidad` | string | no | Muestra la unidad de medida utilizada para contabilizar el producto. |
| `precioMinimo` | number | no | Contiene el costo de venta al público del productom este precio no puede ser menor al costo real del producto. |
| `existencia` | number | no | Guarda la cantidad de productos disponibles. |
| `tkMarca` | string | no | Código que corresponde e identifica de forma única a una marca. ¿Dónde obtengo el token? |
| `tkLinea` | string | no | Código que corresponde e identifica de forma única a una línea de productos. ¿Dónde obtengo el token? |
| `precio1` | number | no | Establece el monto a asignar para la primera lista de precio configurada en el sistema. Se pueden colocar hasta 10 parámetros de precio, ("precio1","precio2","precio3", ...), uno por cada lista de precio configurada en el sistema. Para determinar que lista de precio corresponde a cada parámetro "PRECIO", es necesario obtener el "indiceLista" de las listas de precio. ¿Dónde obtengo el indice de la lista de precio? El monto de mi lista de precio con "indiceLista": "1" , se debe enviar en el parámetro "precio1". El monto de mi lista de precio con "indiceLista": "2" , se debe enviar en el parámetro "precio2". Así sucesivamente. |
| `comision1` | number | no | Establece el monto a asignar para la primera comisión del producto. Se pueden colocar hasta 10 parámetros de comision, ("comision1","comision2","comision3", ...), uno por cada comisión configurada en el sistema. Para determinar que comisión corresponde a cada parámetro "comision", es necesario obtener el "indiceComision" de las comisiones configuradas. ¿Dónde obtengo el indice de las comisiones? El monto de mi comision con "indiceComision": "1" , se debe enviar en el parámetro "comision1". El monto de mi comision con "indiceComision": "2" , se debe enviar en el parámetro "comision2". Así sucesivamente. |
| `impuesto1` | number | no | Establece el monto del primer impuesto trasladado configurado en el sistema. Se pueden colocar hasta 10 parámetros de impuesto, ("impuesto1","impuesto2","impuesto3", ...), uno por cada impuesto configurado en el sistema. Para determinar impuesto corresponde a cada parámetro "impuesto", es necesario obtener el "indiceImpuesto" de los impuestos configurados. ¿Dónde obtengo el indice de los impuestos? El monto de mi impuesto con "indiceImpuesto": "1" , se debe enviar en el parámetro "impuesto1". El monto de mi impuesto con "indiceImpuesto": "2" , se debe enviar en el parámetro "impuesto2". Así sucesivamente. |
| `impuestoR1` | number | no | Establece el monto del primer impuesto retenido configurado en el sistema. Se pueden colocar hasta 10 parámetros de impuestoR, ("impuestoR1","impuestoR2","impuestoR3", ...), uno por cada impuesto configurado en el sistema. Para determinar impuesto corresponde a cada parámetro "impuesto", es necesario obtener el "indiceImpuesto" de los impuestos configurados. ¿Dónde obtengo el indice de los impuestos? El monto de mi impuesto con "indiceImpuesto": "1" , se debe enviar en el parámetro "impuestoR1". El monto de mi impuesto con "indiceImpuesto": "2" , se debe enviar en el parámetro "impuestoR2". Así sucesivamente. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Proporciona un código de verificación como respuesta. |
| `msg` | string | Proporciona un mensaje descriptivo o razón dependiendo el resultado.  - 0 Proceso correcto. - 1 Falló la inserción. - 2 Faltan parámetros. - 3 Error al eliminar el registro. - 4 Token de sesión vencido.  - 5 Fallo de procedimiento en base de datos. - 6 Permisos insuficientes. - 7 Mensajes en la lógica de negocios. |

## Native endpoint

Through the native Upnify API, this operation is `PUT v4/catalogos/productos/:tkProducto` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

