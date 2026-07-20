# Invoice Ninja: Update Quote



```
PUT https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/update-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/update-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "quoteId": "string",
  "clientId": "string",
  "date": "string",
  "dueDate": "string",
  "line_items[0].product_key": "string",
  "line_items[0].quantity": 1,
  "line_items[0].cost": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/update-quote', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "quoteId": "string",
    "clientId": "string",
    "date": "string",
    "dueDate": "string",
    "line_items[0].product_key": "string",
    "line_items[0].quantity": 1,
    "line_items[0].cost": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `quoteId` | string | yes | Hashed quote ID. |
| `clientId` | string | yes | Hashed client ID for the quote. |
| `date` | string | yes | Quote date in YYYY-MM-DD format. |
| `dueDate` | string | yes | Quote due date in YYYY-MM-DD format. |
| `publicNotes` | string | no | Public notes for the quote. |
| `line_items[0].product_key` | string | yes | Product key for the first line item. |
| `line_items[0].quantity` | number | yes | Quantity for the first line item. |
| `line_items[0].cost` | number | yes | Cost for the first line item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "archived_at": 1,
      "balance": 1,
      "client_id": "string",
      "created_at": 1,
      "date": "string",
      "documents": [
        {}
      ],
      "due_date": "string",
      "entity_type": "string",
      "id": "string",
      "invitations": [
        {}
      ],
      "is_deleted": true,
      "line_items": [
        {}
      ],
      "number": "string",
      "public_notes": "string",
      "status_id": "string",
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `archived_at` | number |  |
| `balance` | number |  |
| `client_id` | string |  |
| `created_at` | number |  |
| `date` | string |  |
| `documents` | array<object> |  |
| `due_date` | string |  |
| `entity_type` | string |  |
| `id` | string |  |
| `invitations` | array<object> |  |
| `is_deleted` | boolean |  |
| `line_items` | array<object> |  |
| `number` | string |  |
| `public_notes` | string |  |
| `status_id` | string |  |
| `updated_at` | number |  |

## Native endpoint

Through the native Invoice Ninja API, this operation is `PUT /quotes/:id` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-quote.md) for the provider-specific parameters and requirements.

