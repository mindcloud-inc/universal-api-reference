# Hyperbrowser: Start Browser Use Task



```
POST https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/start-browser-use-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperbrowser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/start-browser-use-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "task": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/start-browser-use-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "task": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `task` | string | yes | Instruction for the browser use task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "liveDomain": "string",
      "liveUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string |  |
| `liveDomain` | string |  |
| `liveUrl` | string |  |

## Native endpoint

Through the native Hyperbrowser API, this operation is `POST /api/task/browser-use` (base URL `https://api.hyperbrowser.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-browser-use-task.md) for the provider-specific parameters and requirements.

