# CustomerX: List Tickets

Retrieves a list of tickets from CustomerX.

```
GET https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-tickets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-tickets?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native CustomerX API, this operation is `GET /api/v1/tickets` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tickets.md) for the provider-specific parameters and requirements.

