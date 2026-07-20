# Charla: List Conversations

Retrieves conversations from Charla.

```
GET https://connect.mindcloud.co/v1/universal/charla/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Charla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/charla/latest/actions/list-conversations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/charla/latest/actions/list-conversations?${params}`, {
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
      "data": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "id": "string",
          "last_message_at": "2026-05-07T12:00:00.000Z",
          "last_seen_at": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "phone": "string"
        }
      ],
      "paging": {
        "has_next": true,
        "next_cursor": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].created_at` | date |  |
| `data[].email` | string |  |
| `data[].id` | string |  |
| `data[].last_message_at` | date |  |
| `data[].last_seen_at` | date |  |
| `data[].name` | string |  |
| `data[].phone` | string |  |
| `paging.has_next` | boolean |  |
| `paging.next_cursor` | number |  |
| `paging.total` | number |  |

## Native endpoint

Through the native Charla API, this operation is `GET /conversations` (base URL `https://api.charla.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

