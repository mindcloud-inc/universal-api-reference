# Rillion Prime Web Service: Set Invoice Payment Date

Register the payment date for an invoice in Prime.

```
PUT https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/set-invoice-payment-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/set-invoice-payment-date" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoicePaymentDate": {},
  "invoicePaymentDate.invoiceSeries": "string",
  "invoicePaymentDate.invoiceNo": 1,
  "invoicePaymentDate.paymentDate": "2026-05-07T12:00:00.000Z",
  "invoicePaymentDate.note": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/set-invoice-payment-date', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoicePaymentDate": {},
    "invoicePaymentDate.invoiceSeries": "string",
    "invoicePaymentDate.invoiceNo": 1,
    "invoicePaymentDate.paymentDate": "2026-05-07T12:00:00.000Z",
    "invoicePaymentDate.note": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoicePaymentDate` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, InvoicePaymentDate section. |
| `invoicePaymentDate.invoiceSeries` | string | yes | Invoice series |
| `invoicePaymentDate.invoiceNo` | number | yes | Invoice number |
| `invoicePaymentDate.paymentDate` | date | yes | Payment date in ERP |
| `invoicePaymentDate.note` | string | yes | Information about the payment e.g. check number. Information will be available on the invoice comment section. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-invoice-payment-date.md) for the provider-specific parameters and requirements.

