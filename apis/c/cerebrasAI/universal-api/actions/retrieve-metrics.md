# Cerebras AI: Retrieve Metrics

Retrieves metrics from Cerebras AI.

```
GET https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/retrieve-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerebras AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/retrieve-metrics?connectionId=$CONNECTION_ID&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/retrieve-metrics?${params}`, {
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
| `organizationId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "model": "string",
      "organizationId": "string",
      "projectId": "string",
      "requests": {},
      "timeWindow": {},
      "tokens": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `model` | string |  |
| `organizationId` | string |  |
| `projectId` | string |  |
| `requests` | object |  |
| `timeWindow` | object |  |
| `tokens` | object |  |

## Native endpoint

Through the native Cerebras AI API, this operation is `GET https://cloud.cerebras.ai/api/v1/metrics/organizations/:organizationId` (base URL `https://api.cerebras.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-metrics.md) for the provider-specific parameters and requirements.

