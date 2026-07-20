# Missive: Create Task

Creates a task in your Missive workspace.

```
POST https://connect.mindcloud.co/v1/universal/missive/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Missive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/missive/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/missive/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Task title. Max 1000 characters. |
| `description` | string | no | Task description. Max 10000 characters. |
| `state` | list | no | Task state. One of: `closed`, `in_progress`, `todo`. |
| `organization` | string | no | Organization ID. Required when using team, assignees, or add_users. |
| `team` | string | no | Team ID. Either team or assignees is required for standalone tasks. |
| `assignees[]` | array<string> | no | Array of assignee user IDs. Either team or assignees is required for standalone tasks. |
| `dueAt` | date | no | Unix timestamp for the task due date. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subtask` | boolean | no | Whether this task is a subtask of a conversation. |
| `conversation` | string | no | Parent conversation ID. Required when subtask is true. |
| `references[]` | array<string> | no | Array of references used to find or create the parent conversation. |
| `conversationSubject` | string | no | Subject for the parent conversation when creating via references. |
| `addUsers[]` | array<string> | no | Array of user IDs to add to the parent conversation. |
| `addToInbox` | boolean | no | Move the parent conversation to Inbox for everyone with access. |

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
        "startedAt": {},
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
| `tasks.startedAt` | object |  |
| `tasks.state` | string |  |
| `tasks.team` | object |  |
| `tasks.title` | string |  |
| `tasks.type` | string |  |

## Native endpoint

Through the native Missive API, this operation is `POST /tasks` (base URL `https://public.missiveapp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

