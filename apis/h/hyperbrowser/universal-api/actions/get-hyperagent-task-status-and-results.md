# Hyperbrowser: Get HyperAgent Task Status and Results



```
GET https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/get-hyperagent-task-status-and-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperbrowser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/get-hyperagent-task-status-and-results?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/get-hyperagent-task-status-and-results?${params}`, {
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
| `id` | string | yes | HyperAgent task identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "error": "string",
      "jobId": "string",
      "jobParams": {},
      "liveDomain": "string",
      "liveUrl": "https://example.com",
      "metadata": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `error` | string |  |
| `jobId` | string |  |
| `jobParams` | object |  |
| `liveDomain` | string |  |
| `liveUrl` | string |  |
| `metadata` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Hyperbrowser API, this operation is `GET /api/task/hyper-agent/:id` (base URL `https://api.hyperbrowser.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hyperagent-task-status-and-results.md) for the provider-specific parameters and requirements.

