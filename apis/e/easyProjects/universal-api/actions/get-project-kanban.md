# Easy Projects: Get Project Kanban

Retrieves the kanban board for an Easy Projects project.

```
GET https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-project-kanban
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Projects `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-project-kanban?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-project-kanban?${params}`, {
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
| `id` | string | yes | Birdview project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerId": 1,
      "id": 1,
      "name": "Ava Chen",
      "projectStatusName": "Ava Chen",
      "statuses": [
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
| `customerId` | number |  |
| `id` | number |  |
| `name` | string |  |
| `projectStatusName` | string |  |
| `statuses` | array<object> |  |

## Native endpoint

Through the native Easy Projects API, this operation is `GET /api/v1/projects/:id/kanban` (base URL `https://api.go.easyprojects.net/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-project-kanban.md) for the provider-specific parameters and requirements.

