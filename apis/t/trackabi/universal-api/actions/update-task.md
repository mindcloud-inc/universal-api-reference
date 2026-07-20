# Trackabi: Update Task

Updates an existing task in Trackabi.

```
PUT https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trackabi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | number | yes | The unique ID of the task. |
| `name` | string | no | Task name. |
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

Through the native Trackabi API, this operation is `PUT /api/v1/tasks/:taskId` (base URL `https://api.trackabi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

