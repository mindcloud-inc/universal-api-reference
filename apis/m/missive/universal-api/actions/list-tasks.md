# Missive: List Tasks

Retrieves tasks from your Missive workspace.

```
GET https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Missive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-tasks?${params}`, {
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
| `organization` | string | no | Filter by organization ID. |
| `team` | string | no | Filter by team ID. |
| `assignee` | string | no | Filter by assignee user ID. |
| `state` | list | no | Filter by task state. One of: `closed`, `in_progress`, `todo`. |
| `type` | list | no | Filter by task type. One of: `all`, `conversation`, `task`. |
| `conversation` | string | no | Filter by parent conversation ID. |
| `dueAtGteq` | date | no | Filter tasks with due_at greater than or equal to this Unix timestamp. |
| `dueAtLteq` | date | no | Filter tasks with due_at less than or equal to this Unix timestamp. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `until` | date | no | Unix timestamp for pagination. Returns tasks with last_activity_at before this value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tasks": [
        {
          "assignees": [
            "string"
          ],
          "closedAt": {},
          "conversation": {},
          "description": "string",
          "dueAt": {},
          "id": "string",
          "lastActivityAt": 1,
          "startedAt": {},
          "state": "string",
          "team": {},
          "title": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tasks[].assignees[]` | string |  |
| `tasks[].closedAt` | object |  |
| `tasks[].conversation` | object |  |
| `tasks[].description` | string |  |
| `tasks[].dueAt` | object |  |
| `tasks[].id` | string |  |
| `tasks[].lastActivityAt` | number |  |
| `tasks[].startedAt` | object |  |
| `tasks[].state` | string |  |
| `tasks[].team` | object |  |
| `tasks[].title` | string |  |
| `tasks[].type` | string |  |

## Native endpoint

Through the native Missive API, this operation is `GET /tasks` (base URL `https://public.missiveapp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

