# Missive: Update Task

Updates a task in your Missive workspace.

```
PUT https://connect.mindcloud.co/v1/universal/missive/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Missive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/missive/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/missive/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Task ID. |
| `title` | string | no | Task title. Max 1000 characters. |
| `description` | string | no | Task description. Max 10000 characters. |
| `state` | list | no | Task state. One of: `closed`, `in_progress`, `todo`. |
| `assignees[]` | array<string> | no | Array of user ID strings. |
| `team` | string | no | Team ID string. |
| `dueAt` | date | no | Unix timestamp for task due date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tasks": {
        "assignees": [
          "string"
        ],
        "closedAt": {},
        "conversation": {},
        "description": "string",
        "dueAt": {},
        "id": "string",
        "startedAt": 1,
        "state": "string",
        "team": {},
        "title": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tasks.assignees[]` | string |  |
| `tasks.closedAt` | object |  |
| `tasks.conversation` | object |  |
| `tasks.description` | string |  |
| `tasks.dueAt` | object |  |
| `tasks.id` | string |  |
| `tasks.startedAt` | number |  |
| `tasks.state` | string |  |
| `tasks.team` | object |  |
| `tasks.title` | string |  |
| `tasks.type` | string |  |

## Native endpoint

Through the native Missive API, this operation is `PATCH /tasks/:id` (base URL `https://public.missiveapp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

