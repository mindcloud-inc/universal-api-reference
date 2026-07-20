# Upnify: Update Sale

Updates an existing sale in Upnify.

```
PUT https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-sale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-sale" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tkVenta": "string",
  "comision": 1,
  "referencia": "string",
  "anticiposMonto": 1,
  "anticiposComision": 1,
  "saldoMonto": 1,
  "parcialidades": 1,
  "cantidad": 1,
  "tkmoneda": "string",
  "tipoDeCambio": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-sale', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tkVenta": "string",
    "comision": 1,
    "referencia": "string",
    "anticiposMonto": 1,
    "anticiposComision": 1,
    "saldoMonto": 1,
    "parcialidades": 1,
    "cantidad": 1,
    "tkmoneda": "string",
    "tipoDeCambio": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tkVenta` | string | yes | El código token que identifica a una venta de manera única dentro del CRM, y a la cual se requiere modificar.. ¿Dónde obtengo el token? |
| `comision` | number | yes | Indica el monto de la comisión ganada. |
| `referencia` | string | yes | Indica la referencia establecida para la venta. |
| `anticiposMonto` | number | yes | Indica un monto de un anticipo. |
| `anticiposComision` | number | yes | Indica el monto de un anticipo. |
| `saldoMonto` | number | yes | Contiene el monto del saldo de la venta en caso de existir anticipos o parcialidades. |
| `parcialidades` | number | yes | Indica el número de parcialidades de una venta. |
| `cantidad` | number | yes | Indica la cantidad de productos de la venta. |
| `tkmoneda` | string | yes | Código token que pertenece a una moneda registrada en el sistema. |
| `tipoDeCambio` | number | yes | Indica el valor de cambio de la moneda utilizada. |

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

Through the native Upnify API, this operation is `PUT v4/ventas/:tkVenta` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sale.md) for the provider-specific parameters and requirements.

