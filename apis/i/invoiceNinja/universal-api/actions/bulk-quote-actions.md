# Invoice Ninja: Bulk Quote Actions



```
PUT https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/bulk-quote-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/bulk-quote-actions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "ids[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/bulk-quote-actions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "ids[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes | Bulk quote action such as approve, convert, send_email, mark_sent, restore, delete, or archive. |
| `ids[]` | array<string> | yes | Array of quote IDs for the bulk action. |

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

Through the native Invoice Ninja API, this operation is `POST /quotes/bulk` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-quote-actions.md) for the provider-specific parameters and requirements.

