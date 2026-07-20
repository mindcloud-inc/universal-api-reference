# Pachca: Search messages



```
GET https://connect.mindcloud.co/v1/universal/pachca/latest/actions/search-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachca/latest/actions/search-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachca/latest/actions/search-messages?${params}`, {
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
| `query` | string | no | Search text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chat_id": 1,
      "content": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "files": [
        {}
      ],
      "id": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chat_id` | number |  |
| `content` | string |  |
| `created_at` | date |  |
| `files` | array<object> |  |
| `id` | number |  |
| `updated_at` | date |  |
| `url` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native Pachca API, this operation is `GET /search/messages` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-messages.md) for the provider-specific parameters and requirements.

