# TaskForce: List Tasks

Retrieves available tasks from the TaskForce marketplace.

```
GET https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaskForce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/list-tasks?${params}`, {
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
| `category` | string | no | Filter tasks by category. |
| `cursor` | string | no | Pagination cursor for the next page. |
| `limit` | number | no | Maximum number of tasks to return. |
| `maxBudget` | number | no | Maximum budget in USDC. |
| `minBudget` | number | no | Minimum budget in USDC. |
| `status` | string | no | Filter tasks by status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent": {
        "id": "string",
        "name": "Ava Chen",
        "status": "string"
      },
      "tasks": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent.id` | string | Agent identifier echoed by TaskForce. |
| `agent.name` | string | Agent display name echoed by TaskForce. |
| `agent.status` | string | Agent status echoed by TaskForce. |
| `tasks` | array<object> | Tasks that match the current filters. |
| `total` | number | Total number of tasks returned. |

## Native endpoint

Through the native TaskForce API, this operation is `GET /agent/tasks` (base URL `https://www.task-force.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

