# Rillion Prime Web Service: Set Invoice Payment Date by UQ

Register the payment date for an invoice identified by its unique key.

```
PUT https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/set-invoice-payment-date-by-uq
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/set-invoice-payment-date-by-uq" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "company": "string",
  "supplier": "string",
  "supplierInvoiceNo": "string",
  "paymentDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/set-invoice-payment-date-by-uq', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "company": "string",
    "supplier": "string",
    "supplierInvoiceNo": "string",
    "paymentDate": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company` | list<string> | yes | Company ID of the invoice. |
| `supplier` | string | yes | Supplier ID of the invoice. |
| `supplierInvoiceNo` | string | yes | Supplier invoice number. |
| `paymentDate` | date | yes | Payment date to register. |
| `note` | string | no | Optional note stored with the payment date. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-invoice-payment-date-by-uq.md) for the provider-specific parameters and requirements.

