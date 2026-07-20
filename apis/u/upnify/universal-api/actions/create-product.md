# Upnify: Create Product

Creates a new product in Upnify.

```
POST https://connect.mindcloud.co/v1/universal/upnify/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idProductoServicioMx": 1,
  "idUnidadMx": 1,
  "codigo": "string",
  "nombre": "string",
  "costo": 1,
  "unidad": "string",
  "precioMinimo": 1,
  "existencia": 1,
  "tkMarca": "string",
  "tkLinea": "string",
  "precio1": 1,
  "comision1": 1,
  "impuesto1": 1,
  "impuestoR1": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upnify/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idProductoServicioMx": 1,
    "idUnidadMx": 1,
    "codigo": "string",
    "nombre": "string",
    "costo": 1,
    "unidad": "string",
    "precioMinimo": 1,
    "existencia": 1,
    "tkMarca": "string",
    "tkLinea": "string",
    "precio1": 1,
    "comision1": 1,
    "impuesto1": 1,
    "impuestoR1": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idProductoServicioMx` | number | yes | Identificador que define el código del catálogo de productos del SAT utilizado. ¿Dónde obtengo el id? |
| `idUnidadMx` | number | yes | Identificador que define el código del catálogo de unidades del SAT. ¿Dónde obtengo el id? |
| `codigo` | string | yes | Contiene un código que puede ser establecido por el usuario para poder identificar el producto en el sistema. |
| `nombre` | string | yes | Guarda el nombre con el que el producto que se registró en el sistema. |
| `costo` | number | yes | Guarda el costo real del producto. |
| `unidad` | string | yes | Muestra la unidad de medida utilizada para contabilizar el producto. |
| `precioMinimo` | number | yes | Contiene el costo de venta al público del producto este precio no puede ser menor al costo real del producto. |
| `existencia` | number | yes | Guarda la cantidad de productos disponibles. |
| `tkMarca` | string | yes | Código que corresponde e identifica de forma única a una marca. ¿Dónde obtengo el token? |
| `tkLinea` | string | yes | Código que corresponde e identifica de forma única a una línea de productos. ¿Dónde obtengo el token? |
| `precio1` | number | yes | Establece el monto a asignar para la primera lista de precio configurada en el sistema. Se pueden colocar hasta 10 parámetros de precio, ("precio1","precio2","precio3", ...), uno por cada lista de precio configurada en el sistema. Para determinar que lista de precio corresponde a cada parámetro "PRECIO", es necesario obtener el "indiceLista" de las listas de precio. ¿Dónde obtengo el indice de la lista de precio? El monto de mi lista de precio con "indiceLista": "1" , se debe enviar en el parámetro "precio1". El monto de mi lista de precio con "indiceLista": "2" , se debe enviar en el parámetro "precio2". Así sucesivamente. |
| `comision1` | number | yes | Establece el monto a asignar para la primera comisión del producto. Se pueden colocar hasta 10 parámetros de comision, ("comision1","comision2","comision3", ...), uno por cada comisión configurada en el sistema. Para determinar que comisión corresponde a cada parámetro "comision", es necesario obtener el "indiceComision" de las comisiones configuradas. ¿Dónde obtengo el indice de las comisiones? El monto de mi comision con "indiceComision": "1" , se debe enviar en el parámetro "comision1". El monto de mi comision con "indiceComision": "2" , se debe enviar en el parámetro "comision2". Así sucesivamente. |
| `impuesto1` | number | yes | Establece el monto del primer impuesto trasladado configurado en el sistema. Se pueden colocar hasta 10 parámetros de impuesto, ("impuesto1","impuesto2","impuesto3", ...), uno por cada impuesto configurado en el sistema. Para determinar impuesto corresponde a cada parámetro "impuesto", es necesario obtener el "indiceImpuesto" de los impuestos configurados. ¿Dónde obtengo el indice de los impuestos? El monto de mi impuesto con "indiceImpuesto": "1" , se debe enviar en el parámetro "impuesto1". El monto de mi impuesto con "indiceImpuesto": "2" , se debe enviar en el parámetro "impuesto2". Así sucesivamente. |
| `impuestoR1` | number | yes | Establece el monto del primer impuesto retenido configurado en el sistema. Se pueden colocar hasta 10 parámetros de impuestoR, ("impuestoR1","impuestoR2","impuestoR3", ...), uno por cada impuesto configurado en el sistema. Para determinar impuesto corresponde a cada parámetro "impuesto", es necesario obtener el "indiceImpuesto" de los impuestos configurados. ¿Dónde obtengo el indice de los impuestos? El monto de mi impuesto con "indiceImpuesto": "1" , se debe enviar en el parámetro "impuestoR1". El monto de mi impuesto con "indiceImpuesto": "2" , se debe enviar en el parámetro "impuestoR2". Así sucesivamente. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "details": "string",
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
| `details` | string | Contiene el token del nuevo registro creado, el nombre de la variable "tkNombreVariable", deberá coincidir con el nombre de la variable que contiene el token del nuevo registro agregado. |
| `msg` | string | Proporciona un mensaje descriptivo o razón dependiendo el resultado.  - 0 Proceso correcto. - 1 Falló la inserción. - 2 Faltan parámetros. - 3 Error al eliminar el registro. - 4 Token de sesión vencido.  - 5 Fallo de procedimiento en base de datos. - 6 Permisos insuficientes. - 7 Mensajes en la lógica de negocios. |

## Native endpoint

Through the native Upnify API, this operation is `POST v4/catalogos/productos` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

