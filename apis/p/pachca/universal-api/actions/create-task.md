# Pachca: Create task



```
POST https://connect.mindcloud.co/v1/universal/pachca/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pachca/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "task": {},
  "task.kind": "reminder"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pachca/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "task": {},
    "task.kind": "reminder"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `task` | object | yes | Task parameters object. |
| `task.kind` | string | yes | Task kind. Use reminder for reminders. Default: `reminder`. |
| `task.content` | string | no | Task description. |
| `task.due_at` | date | no | Task due date in ISO-8601 format. |
| `task.priority` | number | no | Priority: 1, 2, or 3. |
| `task.performer_ids[]` | array<number> | no | User IDs assigned as task performers. Accepts multiple values as an array. |
| `task.chat_id` | number | no | Chat ID to link the task to. |
| `task.all_day` | boolean | no | Whether this is an all-day task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chat_id": 1,
      "content": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "due_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "kind": "string",
      "priority": 1,
      "status": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chat_id` | number |  |
| `content` | string |  |
| `created_at` | date |  |
| `due_at` | date |  |
| `id` | number |  |
| `kind` | string |  |
| `priority` | number |  |
| `status` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native Pachca API, this operation is `POST /tasks` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

