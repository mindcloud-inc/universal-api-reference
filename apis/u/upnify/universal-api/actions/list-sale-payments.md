# Upnify: List Sale Payments

Retrieves payments for a sale in Upnify.

```
GET https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-sale-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-sale-payments?connectionId=$CONNECTION_ID&tkVenta=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tkVenta": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-sale-payments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tkVenta` | string | yes | El código token que identifica a una venta de manera única dentro del CRM, del cual se requiere obtener la lista de los cobros asociados. ¿Dónde obtengo el token? |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auditado": 1,
      "comision": 1,
      "configuracion": "string",
      "emitirComprobante": 1,
      "facturado": 1,
      "facturarPago": 1,
      "fechaHora": "string",
      "fechaProximoEnvio": "string",
      "grupoAuditado": 1,
      "indice": 1,
      "monedaSimbolo": "string",
      "monto": 1,
      "numeroParcialidad": 1,
      "pagado": 1,
      "referencia": "string",
      "statusCobro": "string",
      "tkCobro": "string",
      "tkVenta": "string",
      "ultimaModificacion": "string",
      "unicodeMoneda": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auditado` | number | Código que indica si el cobro se ha auditado. (0-No \|\| 1-Si). |
| `comision` | number | Indica el monto de una comisión. |
| `configuracion` | string | Contiene una cadena de valores codificados en base 64, los cuales mustran la configuración utilizada en el cobro. |
| `emitirComprobante` | number | Código que indica si se requiere emitir un comprobante para el cobro. (0-No \|\| 1-Si). |
| `facturado` | number | Código que indica si el cobro ya ha sido facturado. (0-No \|\| 1-Si). |
| `facturarPago` | number | Código que indica si se requiere facturar el cobro. (0-No \|\| 1-Si). |
| `fechaHora` | string | Contiene un formato compuesto por fehca y hora que indica cuando se realizó el cobro. |
| `fechaProximoEnvio` | string | Contiene un formato de fecha y hora compuesto que indica cuando se realizará el próximo envío. |
| `grupoAuditado` | number | Código que indica si el grupo al que pertenece el vendedor, necesita auditarr las ventas. |
| `indice` | number | Define la posición del registro respecto a los demás registros. |
| `monedaSimbolo` | string | Contiene un símbolo de moneda para el tipo de moneda utilizada. |
| `monto` | number | Contiene el monto del cobro realizado. |
| `numeroParcialidad` | number | Indica la cantidad de parcialidades en las que se cobrará el pago. |
| `pagado` | number | Código que indica si el cobro o el importe a pagar se a cubierto. |
| `referencia` | string | Contiene una descripción que indica desde donde se convierte a venta. |
| `statusCobro` | string | Contiene una descripción que indica el estado actual del cobro. |
| `tkCobro` | string | Contiene un código que identifica de forma única a un cobro en el sistema. |
| `tkVenta` | string | Código token que identifica de forma única a una venta. |
| `ultimaModificacion` | string | Contiene un formato compuesto de fecha y hora que indica cuando se realizó la última modificación del cobro. |
| `unicodeMoneda` | string | Guarda un valor decimal del símbolo de moneda en una tabla unicode. |

## Native endpoint

Through the native Upnify API, this operation is `GET v4/ventas/:tkVenta/cobros` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sale-payments.md) for the provider-specific parameters and requirements.

