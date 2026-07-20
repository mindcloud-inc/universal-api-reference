# Cloro: Create Async Task



```
POST https://connect.mindcloud.co/v1/universal/cloro/latest/actions/create-async-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloro/latest/actions/create-async-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskType": "string",
  "payload": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloro/latest/actions/create-async-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskType": "string",
    "payload": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idempotencyKey` | string | no | Unique string to prevent duplicate task creation. |
| `taskType` | string | yes | The Cloro AI provider task type to run asynchronously. |
| `webhook.url` | string | no | Webhook URL for task completion notification. |
| `payload` | object | yes | Provider-specific request payload. Must include prompt, or query for Google Search. |
| `priority` | number | no | Task priority from 1 to 10. |
| `webhook` | object | no | Webhook configuration for task completion notification. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits": {
        "creditsCharged": 1,
        "creditsToCharge": 1
      },
      "success": true,
      "task": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "idempotencyKey": "string",
        "priority": 1,
        "status": "string",
        "taskType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits.creditsCharged` | number |  |
| `credits.creditsToCharge` | number |  |
| `success` | boolean |  |
| `task.createdAt` | date |  |
| `task.id` | string |  |
| `task.idempotencyKey` | string |  |
| `task.priority` | number |  |
| `task.status` | string |  |
| `task.taskType` | string |  |

## Native endpoint

Through the native Cloro API, this operation is `POST /v1/async/task` (base URL `https://api.cloro.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-async-task.md) for the provider-specific parameters and requirements.

