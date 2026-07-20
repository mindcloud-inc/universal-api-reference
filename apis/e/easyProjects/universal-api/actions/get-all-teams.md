# Easy Projects: Get All Teams

Retrieves teams visible to the current Easy Projects user.

```
GET https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-all-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Projects `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-all-teams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-all-teams?${params}`, {
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
      "avatarUrl": "https://example.com",
      "id": 1,
      "name": "Ava Chen",
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string |  |
| `id` | number |  |
| `name` | string |  |
| `users` | array<object> |  |

## Native endpoint

Through the native Easy Projects API, this operation is `GET /api/v1/teams` (base URL `https://api.go.easyprojects.net/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-teams.md) for the provider-specific parameters and requirements.

