# CustomerX: Create Ticket

Creates a new ticket in CustomerX.

```
POST https://connect.mindcloud.co/v1/universal/customerX/latest/actions/create-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/create-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customerX/latest/actions/create-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "attendant_email": "ava@example.com",
      "attendant_name": "Ava Chen",
      "comment": "string",
      "created_at": "string",
      "date_closing": "string",
      "date_deadline_attendance": "string",
      "date_deadline_closing": "string",
      "date_finalized": "string",
      "date_opening": "string",
      "date_reopening": "string",
      "description": "string",
      "external_id": "string",
      "id": 1,
      "priority": "string",
      "status": "string",
      "title": "string",
      "type_ticket": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendant_email` | string |  |
| `attendant_name` | string |  |
| `comment` | string |  |
| `created_at` | string |  |
| `date_closing` | string |  |
| `date_deadline_attendance` | string |  |
| `date_deadline_closing` | string |  |
| `date_finalized` | string |  |
| `date_opening` | string |  |
| `date_reopening` | string |  |
| `description` | string |  |
| `external_id` | string |  |
| `id` | number |  |
| `priority` | string |  |
| `status` | string |  |
| `title` | string |  |
| `type_ticket` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native CustomerX API, this operation is `POST /api/v1/tickets` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket.md) for the provider-specific parameters and requirements.

