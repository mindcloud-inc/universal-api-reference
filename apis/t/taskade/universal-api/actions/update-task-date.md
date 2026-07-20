# Taskade: Update Task Date

Updates date details for a Taskade task.

```
PUT https://connect.mindcloud.co/v1/universal/taskade/latest/actions/update-task-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Taskade `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/taskade/latest/actions/update-task-date" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "taskId": "string",
  "start.date": "string",
  "start.time": "string",
  "start.timezone": "string",
  "end.date": "string",
  "end.time": "string",
  "end.timezone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/taskade/latest/actions/update-task-date', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "taskId": "string",
    "start.date": "string",
    "start.time": "string",
    "start.timezone": "string",
    "end.date": "string",
    "end.time": "string",
    "end.timezone": "string"
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
| `start.date` | string | yes | Start date. |
| `start.time` | string | yes | Start time. |
| `start.timezone` | string | yes | Start timezone. |
| `end.date` | string | yes | End date. |
| `end.time` | string | yes | End time. |
| `end.timezone` | string | yes | End timezone. |

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

Through the native Taskade API, this operation is `PUT /projects/:projectId/tasks/:taskId/date` (base URL `https://www.taskade.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task-date.md) for the provider-specific parameters and requirements.

