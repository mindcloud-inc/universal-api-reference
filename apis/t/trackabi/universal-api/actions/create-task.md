# Trackabi: Create Task

Creates a new task in a Trackabi project.

```
POST https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trackabi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | The unique ID of the project. |
| `name` | string | yes | Task name. |
| `description` | string | no | Task description. |
| `parentTaskId` | number | no | Parent task. |
| `estimatedTime` | string | no | Estimated time. |
| `startDate` | date | no | Task start date. |
| `endDate` | date | no | Task end date. |
| `notBillable` | number | no | Flag indicating whether the task is billable. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "endDate": "string",
      "estimatedTime": "string",
      "id": 1,
      "name": "Ava Chen",
      "notBillable": "string",
      "parentTaskId": 1,
      "projectId": 1,
      "startDate": "string",
      "subtasksCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `endDate` | string |  |
| `estimatedTime` | string |  |
| `id` | number |  |
| `name` | string |  |
| `notBillable` | string |  |
| `parentTaskId` | number |  |
| `projectId` | number |  |
| `startDate` | string |  |
| `subtasksCount` | number |  |

## Native endpoint

Through the native Trackabi API, this operation is `POST /api/v1/projects/:projectId/tasks` (base URL `https://api.trackabi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

