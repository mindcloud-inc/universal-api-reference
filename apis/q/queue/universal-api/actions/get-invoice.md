# Queue: Get Invoice

Retrieves an invoice from Queue.

```
GET https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Queue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-invoice?connectionId=$CONNECTION_ID&invoiceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-invoice?${params}`, {
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
| `invoiceId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "amount": 1,
      "billFrom": "string",
      "billTo": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditType": "string",
      "due": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "invoiceItems": [
        {}
      ],
      "invoiceNumber": "string",
      "issued": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "paymentMethod": "string",
      "paymentTerms": "string",
      "recurringInvoiceItems": [
        {}
      ],
      "tax": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `amount` | number |  |
| `billFrom` | string |  |
| `billTo` | string |  |
| `createdAt` | date |  |
| `creditType` | string |  |
| `due` | date |  |
| `id` | string |  |
| `invoiceItems` | array<object> |  |
| `invoiceNumber` | string |  |
| `issued` | date |  |
| `name` | string |  |
| `paymentMethod` | string |  |
| `paymentTerms` | string |  |
| `recurringInvoiceItems` | array<object> |  |
| `tax` | number |  |
| `updatedAt` | date |  |
| `user` | object |  |

## Native endpoint

Through the native Queue API, this operation is `GET invoices/:invoice_id` (base URL `https://app.usequeue.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

