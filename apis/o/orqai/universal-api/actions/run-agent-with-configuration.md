# Orq.ai: Run Agent With Configuration

Runs an agent with custom configuration in Orq.ai.

```
POST https://connect.mindcloud.co/v1/universal/orqai/latest/actions/run-agent-with-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/run-agent-with-configuration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orqai/latest/actions/run-agent-with-configuration', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "contextId": "string",
      "id": "string",
      "kind": "string",
      "status": {
        "state": "string",
        "timestamp": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contextId` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `status.state` | string |  |
| `status.timestamp` | string |  |

## Native endpoint

Through the native Orq.ai API, this operation is `POST /v2/agents/run` (base URL `https://api.orq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-agent-with-configuration.md) for the provider-specific parameters and requirements.

