# Mendato: Create Invoice



```
POST https://connect.mindcloud.co/v1/universal/mendato/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mendato/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | yes | GraphQL variables object for the Mendato create invoice mutation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createInvoice": {
        "invoice": {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "dueDate": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "invoiceDate": "2026-05-07T12:00:00.000Z",
          "isNegative": true,
          "number": 1,
          "numberPrefix": "string",
          "numberSuffix": "string",
          "status": "string",
          "totalAmount": 1,
          "totalNetAmount": 1,
          "type": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createInvoice.invoice.createdAt` | date |  |
| `createInvoice.invoice.dueDate` | date |  |
| `createInvoice.invoice.id` | string |  |
| `createInvoice.invoice.invoiceDate` | date |  |
| `createInvoice.invoice.isNegative` | boolean |  |
| `createInvoice.invoice.number` | number |  |
| `createInvoice.invoice.numberPrefix` | string |  |
| `createInvoice.invoice.numberSuffix` | string |  |
| `createInvoice.invoice.status` | string |  |
| `createInvoice.invoice.totalAmount` | number |  |
| `createInvoice.invoice.totalNetAmount` | number |  |
| `createInvoice.invoice.type` | string |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

