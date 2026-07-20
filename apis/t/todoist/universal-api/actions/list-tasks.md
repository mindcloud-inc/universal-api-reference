# Todoist: List Tasks

Retrieves tasks from Todoist.

```
GET https://connect.mindcloud.co/v1/universal/todoist/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Todoist `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/todoist/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/todoist/latest/actions/list-tasks?${params}`, {
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
| `projectId` | string | no |  |
| `sectionId` | string | no |  |
| `label` | string | no |  |
| `filter` | string | no | Natural language filter query for selecting tasks. |
| `ids` | list<string> | no | Comma-separated task IDs to fetch specific tasks. |
| `parentId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextCursor": "string",
      "results": [
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
| `nextCursor` | string | Pagination cursor for next page. |
| `results` | array<object> | Active task results array. |

## Native endpoint

Through the native Todoist API, this operation is `GET /api/v1/tasks` (base URL `https://api.todoist.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

