# Unleash: Get projects

Retrieves projects from Unleash.

```
GET https://connect.mindcloud.co/v1/universal/unleash/latest/actions/get-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleash `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unleash/latest/actions/get-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleash/latest/actions/get-projects?${params}`, {
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
      "defaultStickiness": "string",
      "description": "string",
      "featureCount": 1,
      "health": 1,
      "id": "string",
      "memberCount": 1,
      "mode": "string",
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
| `createdAt` | date | Creation timestamp. |
| `defaultStickiness` | string | Default stickiness setting for feature strategies. |
| `description` | string | Project description. |
| `featureCount` | number | Number of feature flags in the project. |
| `health` | number | Project health score. |
| `id` | string | Project identifier. |
| `memberCount` | number | Number of project members. |
| `mode` | string | Project collaboration mode. |
| `name` | string | Project display name. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Unleash API, this operation is `GET /api/admin/projects` (base URL `https://us.app.getunleash.io/uspp0456`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-projects.md) for the provider-specific parameters and requirements.

