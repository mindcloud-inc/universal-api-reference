# Cloro: Create Batch Tasks



```
POST https://connect.mindcloud.co/v1/universal/cloro/latest/actions/create-batch-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloro/latest/actions/create-batch-tasks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tasks[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloro/latest/actions/create-batch-tasks', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tasks[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tasks[]` | array<object> | yes | Array of async task definitions to create in one batch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "credits": {
            "creditsToCharge": 1
          },
          "index": 1,
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
      "success": true,
      "summary": {
        "failed": 1,
        "succeeded": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results[].credits.creditsToCharge` | number |  |
| `results[].index` | number |  |
| `results[].success` | boolean |  |
| `results[].task.createdAt` | date |  |
| `results[].task.id` | string |  |
| `results[].task.idempotencyKey` | string |  |
| `results[].task.priority` | number |  |
| `results[].task.status` | string |  |
| `results[].task.taskType` | string |  |
| `success` | boolean |  |
| `summary.failed` | number |  |
| `summary.succeeded` | number |  |
| `summary.total` | number |  |

## Native endpoint

Through the native Cloro API, this operation is `POST /v1/async/task/batch` (base URL `https://api.cloro.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-batch-tasks.md) for the provider-specific parameters and requirements.

