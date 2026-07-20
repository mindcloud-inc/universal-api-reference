# Upnify: Update Opportunity

Updates an existing opportunity in Upnify.

```
PUT https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tkOportunidad": "string",
  "tkFase": "string",
  "tkLineaProducto": "string",
  "tkMoneda": "string",
  "tkCerteza": "string",
  "concepto": "string",
  "cierreEstimado": "2026-05-07T12:00:00.000Z",
  "monto": 1,
  "cantidad": 1,
  "subtotal": 1,
  "comision": 1,
  "comisionMonto": 1,
  "descuento": 1,
  "descuentoPct": 1,
  "impuestos": 1,
  "impuestosRetenidos": 1,
  "productos": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-opportunity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tkOportunidad": "string",
    "tkFase": "string",
    "tkLineaProducto": "string",
    "tkMoneda": "string",
    "tkCerteza": "string",
    "concepto": "string",
    "cierreEstimado": "2026-05-07T12:00:00.000Z",
    "monto": 1,
    "cantidad": 1,
    "subtotal": 1,
    "comision": 1,
    "comisionMonto": 1,
    "descuento": 1,
    "descuentoPct": 1,
    "impuestos": 1,
    "impuestosRetenidos": 1,
    "productos": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tkOportunidad` | string | yes | El código token que identifica a una oportunidad de manera única dentro del CRM, la cual se requiere modificar. ¿Dónde obtengo el token? |
| `tkFase` | string | yes | Código token que identificade forma única a una fase en el sistema. ¿Dónde obtengo el token? |
| `tkLineaProducto` | string | yes | Código token que identificade forma única a una línea de productos en el sistema. ¿Dónde obtengo el token? |
| `tkMoneda` | string | yes | Código token que identificade forma única a un tipo de moneda en el sistema. ¿Dónde obtengo el token? |
| `tkCerteza` | string | yes | Código token que identificade forma única a una certeza en el sistema. ¿Dónde obtengo el token? |
| `concepto` | string | yes | Contiene el título o nombre de la nueva oportunidad. |
| `cierreEstimado` | date | yes | Contiene un formato compuesto de fecha y hora que indica la fecha estimada en la que se concretará la oportunidad. |
| `monto` | number | yes | Almacena una cantidad monetaria que indica el monto de la oportunidad. |
| `cantidad` | number | yes | Almacena la cantidad total de productos vendidos. |
| `subtotal` | number | yes | Almacena una cantidad monetaria que indica el subtotal de la oportunidad. |
| `comision` | number | yes | Almacena un valor con base 1, donde 1 es el 100%. Este valor indica el porcentaje de una comisión. |
| `comisionMonto` | number | yes | Indica la cantidad monetaria de la comisión. |
| `descuento` | number | yes | Indica la cantidad monetaria del descuento realizado a la oportunidad. |
| `descuentoPct` | number | yes | Almacena un valor con base 1, donde 1 es el 100%. Este valor indica el porcentaje del descuento. |
| `impuestos` | number | yes | Almacena una cantidad monetaria que indica el monto total de los impuestos trasladados de la oportunidad. |
| `impuestosRetenidos` | number | yes | Almacena una cantidad monetaria que indica el monto total de los impuestos retenidos de la oportunidad. |
| `productos` | object | yes | Arreglo de datos en las que se agregan los productos relacionados a la oportunidad. |

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
| `code` | number | Proporciona un código de verificación como respuesta.  - 0 Proceso correcto. - 1 Falló la inserción. - 2 Faltan parámetros. - 3 Error al eliminar el registro. - 4 Token de sesión vencido.  - 5 Fallo de procedimiento en base de datos. - 6 Permisos insuficientes. - 7 Mensajes en la lógica de negocios. |
| `details` | string | Contiene el token del nuevo registro creado, el nombre de la variable "tkNombreVariable", deberá coincidir con el nombre de la variable que contiene el token del nuevo registro agregado. |
| `msg` | string | Proporciona un mensaje descriptivo o razón dependiendo el resultado. |

## Native endpoint

Through the native Upnify API, this operation is `PUT v4/oportunidades/:tkOportunidad` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-opportunity.md) for the provider-specific parameters and requirements.

