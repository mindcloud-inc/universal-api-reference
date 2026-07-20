# Dribbble: List User Projects



```
GET https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/list-user-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dribbble `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/list-user-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/list-user-projects?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "shotsCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `shotsCount` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Dribbble API, this operation is `GET /user/projects` (base URL `https://api.dribbble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-projects.md) for the provider-specific parameters and requirements.

