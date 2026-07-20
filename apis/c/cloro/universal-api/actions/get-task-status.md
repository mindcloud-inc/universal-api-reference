# Cloro: Get Task Status



```
GET https://connect.mindcloud.co/v1/universal/cloro/latest/actions/get-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloro/latest/actions/get-task-status?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloro/latest/actions/get-task-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The Cloro async task ID to retrieve. |

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
      "response": {
        "model": "string",
        "text": "string"
      },
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
| `response.model` | string |  |
| `response.text` | string |  |
| `task.createdAt` | date |  |
| `task.id` | string |  |
| `task.idempotencyKey` | string |  |
| `task.priority` | number |  |
| `task.status` | string |  |
| `task.taskType` | string |  |

## Native endpoint

Through the native Cloro API, this operation is `GET /v1/async/task/:taskId` (base URL `https://api.cloro.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-status.md) for the provider-specific parameters and requirements.

