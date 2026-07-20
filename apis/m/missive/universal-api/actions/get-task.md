# Missive: Get Task

Retrieves a task from your Missive workspace.

```
GET https://connect.mindcloud.co/v1/universal/missive/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Missive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/missive/latest/actions/get-task?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/missive/latest/actions/get-task?${params}`, {
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
| `id` | string | yes | Task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tasks": {
        "assignees": [
          {
            "avatarUrl": "https://example.com",
            "email": "ava@example.com",
            "id": "string",
            "name": "Ava Chen"
          }
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
| `tasks.assignees[].avatarUrl` | string |  |
| `tasks.assignees[].email` | string |  |
| `tasks.assignees[].id` | string |  |
| `tasks.assignees[].name` | string |  |
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

Through the native Missive API, this operation is `GET /tasks/:id` (base URL `https://public.missiveapp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

