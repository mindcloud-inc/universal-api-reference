# Insighto.ai: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insighto.ai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-contacts?${params}`, {
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
      "channels": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_fields": {},
      "email": "ava@example.com",
      "first_assistant_id": "string",
      "first_name": "Ava",
      "first_widget_id": "string",
      "id": "string",
      "last_assistant_id": "string",
      "last_name": "Chen",
      "last_seen": "2026-05-07T12:00:00.000Z",
      "last_sent": "2026-05-07T12:00:00.000Z",
      "last_widget_id": "string",
      "org_id": "string",
      "user_attributes": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels` | object |  |
| `created_at` | date |  |
| `custom_fields` | object |  |
| `email` | string |  |
| `first_assistant_id` | string |  |
| `first_name` | string |  |
| `first_widget_id` | string |  |
| `id` | string |  |
| `last_assistant_id` | string |  |
| `last_name` | string |  |
| `last_seen` | date |  |
| `last_sent` | date |  |
| `last_widget_id` | string |  |
| `org_id` | string |  |
| `user_attributes` | object |  |

## Native endpoint

Through the native Insighto.ai API, this operation is `GET /contact` (base URL `https://api.insighto.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

