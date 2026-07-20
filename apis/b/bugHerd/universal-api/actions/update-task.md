# BugHerd: Update Task

Updates an existing task in BugHerd.

```
PUT https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BugHerd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "taskId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "taskId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | The BugHerd project ID. |
| `taskId` | number | yes | The BugHerd task ID. |
| `task` | object | no | Task fields to update. |
| `task.priority` | string | no | The BugHerd task priority. |
| `task.status` | string | no | The target task status or column name. |
| `task.assigned_to_id` | number | no | Assign the task to a BugHerd user ID. |
| `task.updater_email` | string | no | Audit-log the update as this email address. |
| `task.unassign_user` | number | no | Unassign a specific user ID from the task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminLink": "https://example.com",
      "columnId": 1,
      "description": "string",
      "id": 1,
      "localTaskId": 1,
      "priority": "string",
      "projectId": 1,
      "projectName": "Ava Chen",
      "secretLink": "https://example.com",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminLink` | string |  |
| `columnId` | number |  |
| `description` | string |  |
| `id` | number |  |
| `localTaskId` | number |  |
| `priority` | string |  |
| `projectId` | number |  |
| `projectName` | string |  |
| `secretLink` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native BugHerd API, this operation is `PUT projects/:project_id/tasks/:task_id.json` (base URL `https://www.bugherd.com/api_v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

