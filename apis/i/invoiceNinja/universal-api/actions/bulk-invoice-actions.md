# Invoice Ninja: Bulk Invoice Actions



```
PUT https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/bulk-invoice-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/bulk-invoice-actions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "ids": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/bulk-invoice-actions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "ids": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes | Bulk action such as mark_sent, archive, delete, or email. |
| `ids` | list<string> | yes | Array of invoice ids to act on. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailType` | string | no | Email template type when emailing invoices. |

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

Through the native Invoice Ninja API, this operation is `POST /invoices/bulk` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-invoice-actions.md) for the provider-specific parameters and requirements.

