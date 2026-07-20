# FireHydrant: Update Incident Task

Updates an existing incident task in FireHydrant.

```
PUT https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/update-incident-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FireHydrant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/update-incident-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "incidentId": "string",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/update-incident-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "incidentId": "string",
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assigneeId` | string | no | The user ID assigned to the task. |
| `description` | string | no | Task description. |
| `dueAt` | string | no | Task due date or relative time like 5m. |
| `incidentId` | string | yes | The FireHydrant incident ID. |
| `title` | string | no | The task title. |
| `taskId` | string | yes | The FireHydrant incident task ID. |
| `state` | list | no | Task state: open, in_progress, cancelled, or done. One of: `0`, `1`, `2`, `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "description": "string",
      "dueAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "state": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee` | object |  |
| `createdAt` | date |  |
| `createdBy` | object |  |
| `description` | string |  |
| `dueAt` | date |  |
| `id` | string |  |
| `state` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native FireHydrant API, this operation is `PATCH /incidents/:incident_id/tasks/:task_id` (base URL `https://api.firehydrant.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-incident-task.md) for the provider-specific parameters and requirements.

