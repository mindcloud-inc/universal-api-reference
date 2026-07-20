# Pachca: List users



```
GET https://connect.mindcloud.co/v1/universal/pachca/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachca/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachca/latest/actions/list-users?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "department": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "image_url": "https://example.com",
      "last_name": "Chen",
      "role": "string",
      "suspended": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `department` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | number |  |
| `image_url` | string |  |
| `last_name` | string |  |
| `role` | string |  |
| `suspended` | boolean |  |
| `title` | string |  |

## Native endpoint

Through the native Pachca API, this operation is `GET /users` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

