# Pachca: List chats



```
GET https://connect.mindcloud.co/v1/universal/pachca/latest/actions/list-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachca/latest/actions/list-chats?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachca/latest/actions/list-chats?${params}`, {
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
      "chat_subtype": "string",
      "chat_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "member_count": 1,
      "name": "Ava Chen",
      "owner_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chat_subtype` | string |  |
| `chat_type` | string |  |
| `created_at` | date |  |
| `id` | number |  |
| `member_count` | number |  |
| `name` | string |  |
| `owner_id` | number |  |

## Native endpoint

Through the native Pachca API, this operation is `GET /chats` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-chats.md) for the provider-specific parameters and requirements.

