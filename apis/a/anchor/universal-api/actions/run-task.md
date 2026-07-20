# Anchor: Run Task

Creates a task run in Anchor.

```
POST https://connect.mindcloud.co/v1/universal/anchor/latest/actions/run-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anchor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anchor/latest/actions/run-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputParams": {},
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anchor/latest/actions/run-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputParams": {},
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputParams` | object | yes |  |
| `taskId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "result": {},
      "run_id": "string",
      "session_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `result` | object |  |
| `run_id` | string |  |
| `session_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Anchor API, this operation is `POST /v2/tasks/:taskId/run` (base URL `https://api.anchorbrowser.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-task.md) for the provider-specific parameters and requirements.

