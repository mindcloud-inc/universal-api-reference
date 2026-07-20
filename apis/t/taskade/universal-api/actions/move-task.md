# Taskade: Move Task

Moves a task within a Taskade project.

```
PUT https://connect.mindcloud.co/v1/universal/taskade/latest/actions/move-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Taskade `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/taskade/latest/actions/move-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "taskId": "string",
  "target.taskId": "string",
  "target.position": "beforebegin"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/taskade/latest/actions/move-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "taskId": "string",
    "target.taskId": "string",
    "target.position": "beforebegin"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Project ID. |
| `taskId` | string | yes | Task ID. |
| `target.taskId` | string | yes | Target task ID. |
| `target.position` | string | yes | Relative insertion position. Default: `beforebegin`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed` | boolean | Whether the task is completed. |
| `id` | string | Task ID. |

## Native endpoint

Through the native Taskade API, this operation is `PUT /projects/:projectId/tasks/:taskId/move` (base URL `https://www.taskade.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-task.md) for the provider-specific parameters and requirements.

