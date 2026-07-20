# HoneyHive: Get Metrics

Retrieves a list of metrics from HoneyHive.

```
GET https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoneyHive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-metrics?connectionId=$CONNECTION_ID&projectName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-metrics?${params}`, {
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
| `projectName` | string | yes | Project name associated with metrics. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "childMetrics": [
        {}
      ],
      "codeSnippet": "string",
      "criteria": "string",
      "description": "string",
      "enabledInProd": true,
      "eventName": "Ava Chen",
      "eventType": "string",
      "id": "string",
      "modelName": "Ava Chen",
      "modelProvider": "string",
      "name": "Ava Chen",
      "needsGroundTruth": true,
      "passWhen": true,
      "prompt": "string",
      "returnType": "string",
      "task": "string",
      "threshold": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `childMetrics` | array<object> |  |
| `codeSnippet` | string |  |
| `criteria` | string |  |
| `description` | string |  |
| `enabledInProd` | boolean |  |
| `eventName` | string |  |
| `eventType` | string |  |
| `id` | string |  |
| `modelName` | string |  |
| `modelProvider` | string |  |
| `name` | string |  |
| `needsGroundTruth` | boolean |  |
| `passWhen` | boolean |  |
| `prompt` | string |  |
| `returnType` | string |  |
| `task` | string |  |
| `threshold` | object |  |
| `type` | string |  |

## Native endpoint

Through the native HoneyHive API, this operation is `GET /metrics` (base URL `https://api.honeyhive.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-metrics.md) for the provider-specific parameters and requirements.

