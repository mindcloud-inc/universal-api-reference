# Pachca: Update task



```
PUT https://connect.mindcloud.co/v1/universal/pachca/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pachca/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "task": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pachca/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "task": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Pachca task ID. |
| `task` | object | yes | Task parameters object. |
| `task.content` | string | no | Task description. |
| `task.status` | string | no | Task status. |
| `task.due_at` | date | no | Task due date in ISO-8601 format. |
| `task.priority` | number | no | Priority: 1, 2, or 3. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chat_id": 1,
      "content": "string",
      "due_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "kind": "string",
      "priority": 1,
      "status": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
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
| `due_at` | date |  |
| `id` | number |  |
| `kind` | string |  |
| `priority` | number |  |
| `status` | string |  |
| `updated_at` | date |  |
| `user_id` | number |  |

## Native endpoint

Through the native Pachca API, this operation is `PUT /tasks/{id}` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

