# Invoice Ninja: Create Quote



```
POST https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/create-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/create-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "string",
  "date": "2026-03-20",
  "dueDate": "2026-03-27",
  "line_items[0].product_key": "string",
  "line_items[0].quantity": 1,
  "line_items[0].cost": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/create-quote', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "string",
    "date": "2026-03-20",
    "dueDate": "2026-03-27",
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
| `clientId` | string | yes | Hashed client ID for the quote. |
| `date` | string | yes | Quote date in YYYY-MM-DD format. Example: `2026-03-20`. |
| `dueDate` | string | yes | Quote due date in YYYY-MM-DD format. Example: `2026-03-27`. |
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

Through the native Invoice Ninja API, this operation is `POST /quotes` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-quote.md) for the provider-specific parameters and requirements.

