# Invoice Ninja: Show Quote



```
GET https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/show-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/show-quote?connectionId=$CONNECTION_ID&quoteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "quoteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/show-quote?${params}`, {
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
| `quoteId` | string | yes | Hashed quote ID. |

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

Through the native Invoice Ninja API, this operation is `GET /quotes/:id` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-quote.md) for the provider-specific parameters and requirements.

