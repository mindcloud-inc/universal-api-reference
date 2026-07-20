# Zoho Connect: Complete Task

Completes a task in Zoho Connect.

```
PUT https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/complete-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/complete-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scopeID": "string",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/complete-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scopeID": "string",
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scopeID` | string | yes | ID of the network where the task exists. |
| `taskId` | string | yes | ID of the task to complete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completeTask": {
        "completedBy": {
          "id": "string",
          "name": "Ava Chen"
        },
        "completedTime": "string",
        "id": "string",
        "isCompleted": true,
        "result": "string",
        "taskPercentage": 1,
        "taskStatus": {
          "id": "string",
          "name": "Ava Chen"
        },
        "timeTakenToComplete": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completeTask.completedBy.id` | string |  |
| `completeTask.completedBy.name` | string |  |
| `completeTask.completedTime` | string |  |
| `completeTask.id` | string |  |
| `completeTask.isCompleted` | boolean |  |
| `completeTask.result` | string |  |
| `completeTask.taskPercentage` | number |  |
| `completeTask.taskStatus.id` | string |  |
| `completeTask.taskStatus.name` | string |  |
| `completeTask.timeTakenToComplete` | string |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `POST /pulse/api/completeTask` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-task.md) for the provider-specific parameters and requirements.

