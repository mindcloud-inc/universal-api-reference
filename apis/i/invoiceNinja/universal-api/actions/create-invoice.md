# Invoice Ninja: Create Invoice



```
POST https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | yes | The client hashed id. |
| `date` | string | no | The invoice date in YYYY-MM-DD format. |
| `dueDate` | string | no | The due date in YYYY-MM-DD format. |
| `lineItems` | list<object> | no | Array of invoice line item objects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "archivedAt": 1,
      "autoBillEnabled": true,
      "backup": {},
      "balance": 1,
      "clientId": "string",
      "createdAt": 1,
      "date": "string",
      "documents": [
        {}
      ],
      "dueDate": "string",
      "eInvoice": {},
      "entityType": "string",
      "id": "string",
      "invitations": [
        {}
      ],
      "isDeleted": true,
      "lineItems": [
        {}
      ],
      "number": "string",
      "paidToDate": 1,
      "privateNotes": "string",
      "publicNotes": "string",
      "statusId": "string",
      "taxInfo": {},
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `archivedAt` | number |  |
| `autoBillEnabled` | boolean |  |
| `backup` | object |  |
| `balance` | number |  |
| `clientId` | string |  |
| `createdAt` | number |  |
| `date` | string |  |
| `documents` | array<object> |  |
| `dueDate` | string |  |
| `eInvoice` | object |  |
| `entityType` | string |  |
| `id` | string |  |
| `invitations` | array<object> |  |
| `isDeleted` | boolean |  |
| `lineItems` | array<object> |  |
| `number` | string |  |
| `paidToDate` | number |  |
| `privateNotes` | string |  |
| `publicNotes` | string |  |
| `statusId` | string |  |
| `taxInfo` | object |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Invoice Ninja API, this operation is `POST /invoices` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

