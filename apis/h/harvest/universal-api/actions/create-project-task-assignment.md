# Harvest: Create Project Task Assignment

Creates a task assignment for a project in Harvest.

```
POST https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-project-task-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-project-task-assignment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "taskId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-project-task-assignment', {
  method: 'POST',
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
| `projectId` | number | yes |  |
| `taskId` | number | yes |  |
| `isActive` | boolean | no |  |
| `billable` | boolean | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hourlyRate` | number | no |  |
| `budget` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": true,
      "budget": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "hourlyRate": 1,
      "id": 1,
      "isActive": true,
      "project": {},
      "task": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | boolean |  |
| `budget` | number |  |
| `createdAt` | date |  |
| `hourlyRate` | number |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `project` | object |  |
| `task` | object |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Harvest API, this operation is `POST /v2/projects/:projectId/task_assignments` (base URL `https://api.harvestapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-task-assignment.md) for the provider-specific parameters and requirements.

