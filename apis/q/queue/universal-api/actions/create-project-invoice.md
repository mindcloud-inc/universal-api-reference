# Queue: Create Project Invoice

Creates a new invoice for a Queue project.

```
POST https://connect.mindcloud.co/v1/universal/queue/latest/actions/create-project-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Queue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/queue/latest/actions/create-project-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/queue/latest/actions/create-project-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes |  |
| `billTo` | string | no |  |
| `address` | string | no |  |
| `tax` | number | no |  |
| `paymentTerms` | string | no |  |
| `due` | string | no |  |
| `paymentMethod` | string | no |  |
| `invoiceNumber` | number | no |  |
| `currency` | string | no |  |
| `creditType` | boolean | no |  |

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

Through the native Queue API, this operation is `POST projects/:project_id/invoices` (base URL `https://app.usequeue.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-invoice.md) for the provider-specific parameters and requirements.

