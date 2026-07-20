# Circle: List Topics

Retrieves topic records from your Circle community.

```
GET https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-topics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-topics?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-topics?${params}`, {
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
      "adminOnly": true,
      "author": {
        "avatarUrl": "https://example.com",
        "firstName": "Ava",
        "lastName": "Chen"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminOnly` | boolean |  |
| `author.avatarUrl` | string |  |
| `author.firstName` | string |  |
| `author.lastName` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `name` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Circle API, this operation is `GET /api/admin/v2/topics` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-topics.md) for the provider-specific parameters and requirements.

