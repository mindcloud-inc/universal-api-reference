# Upnify: Create Sale

Creates a new sale in Upnify.

```
POST https://connect.mindcloud.co/v1/universal/upnify/latest/actions/create-sale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/create-sale" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tkProspecto": "string",
  "tkFase": "string",
  "tkLineaProducto": "string",
  "tkMoneda": "string",
  "tkCerteza": "string",
  "concepto": "string",
  "cantidad": 1,
  "referencia": "string",
  "fechaCierreVenta": "2026-05-07T12:00:00.000Z",
  "monto": 1,
  "anticiposMonto": 1,
  "anticiposComision": 1,
  "comision": 1,
  "comisionMonto": 1,
  "saldoMonto": 1,
  "saldoComision": 1,
  "productos": {},
  "pagos": {},
  "tipoDeCambio": 1,
  "tipoComision": 1,
  "parcialidades": 1,
  "periodicidad": 1,
  "montoPagado": 1,
  "descuento": 1,
  "descuentoPct": 1,
  "subtotal": 1,
  "impuestos": 1,
  "impuestosRetenidos": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upnify/latest/actions/create-sale', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tkProspecto": "string",
    "tkFase": "string",
    "tkLineaProducto": "string",
    "tkMoneda": "string",
    "tkCerteza": "string",
    "concepto": "string",
    "cantidad": 1,
    "referencia": "string",
    "fechaCierreVenta": "2026-05-07T12:00:00.000Z",
    "monto": 1,
    "anticiposMonto": 1,
    "anticiposComision": 1,
    "comision": 1,
    "comisionMonto": 1,
    "saldoMonto": 1,
    "saldoComision": 1,
    "productos": {},
    "pagos": {},
    "tipoDeCambio": 1,
    "tipoComision": 1,
    "parcialidades": 1,
    "periodicidad": 1,
    "montoPagado": 1,
    "descuento": 1,
    "descuentoPct": 1,
    "subtotal": 1,
    "impuestos": 1,
    "impuestosRetenidos": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tkProspecto` | string | yes | Código token del prospecto al que se agregará la venta. ¿Dónde obtengo el token? |
| `tkFase` | string | yes | Código token que identificade forma única a una fase en el sistema. ¿Dónde obtengo el token? |
| `tkLineaProducto` | string | yes | Código token que identificade forma única a una línea de productos en el sistema. ¿Dónde obtengo el token? |
| `tkMoneda` | string | yes | Código token que identificade forma única a un tipo de moneda en el sistema. ¿Dónde obtengo el token? |
| `tkCerteza` | string | yes | Código token que identificade forma única a una certeza en el sistema. ¿Dónde obtengo el token? |
| `concepto` | string | yes | Identifica el concepto de la oportunidad. |
| `cantidad` | number | yes | Identifica la cantidad de productos/servicios de la venta. |
| `referencia` | string | yes | Identifica el motivo de la venta. |
| `fechaCierreVenta` | date | yes | Contiene un formato compuesto por fecha y hora que indica cuando se realizó la venta. |
| `monto` | number | yes | Cantidad monetaria con la que se generará la venta. |
| `anticiposMonto` | number | yes | Cantidad monetaria que indica el monto que estan pagando de la venta. |
| `anticiposComision` | number | yes | Cantidad monetaria que indica el monto que estan pagando de la comision de la venta. |
| `comision` | number | yes | Indica una cantidad de comision con base 1, (donde 1 es el 100%)por el la venta. |
| `comisionMonto` | number | yes | Cantidad monetaria que indica el monto total de comisión por la venta. |
| `saldoMonto` | number | yes | Cantidad monetaría que identifica el saldo pendiente de la venta. |
| `saldoComision` | number | yes | Cantidad monetaría que identifica el saldo pendiente de la comisión por la venta. |
| `productos` | object | yes | Arreglo de datos en las que se agregan los productos relacionados a la venta. |
| `pagos` | object | yes | Arreglo de datos en las que se agregan los pagos relacionados a la venta. |
| `tipoDeCambio` | number | yes | Indica el tipo de cambio con el que se generará la venta. |
| `tipoComision` | number | yes | Indica la forma en la que se pagarán las comisiones. - 0 Prorrateadas. - 1 Primer pago. - 2 Último pago. - 3 Manual. |
| `parcialidades` | number | yes | Indica el numero de parcialidades en las que se liquidará la venta. |
| `periodicidad` | number | yes | Indica la forma en la que se realizaran los pagos de la venta - 1 Mensual. - 2 Bimestral. - 3 Trimestral. - 4 Semestral. - 5 Anual. - 6 Otro. - 7 Semanal. - 8 Quincenal. |
| `montoPagado` | number | yes | Indica el monto que se esta pagando de la venta. |
| `descuento` | number | yes | Indica la cantidad monetaria del descuento realizado a la venta. |
| `descuentoPct` | number | yes | Almacena un valor con base 1, donde 1 es el 100%. Este valor indica el porcentaje del descuento. |
| `subtotal` | number | yes | Almacena una cantidad monetaria que indica el subtotal de la venta. |
| `impuestos` | number | yes | Almacena una cantidad monetaria que indica el monto total de los impuestos trasladados de la venta. |
| `impuestosRetenidos` | number | yes | Almacena una cantidad monetaria que indica el monto total de los impuestos retenidos de la venta. |

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

Through the native Upnify API, this operation is `POST v4/ventas` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sale.md) for the provider-specific parameters and requirements.

