# Bolna: Patch Update Agent

Updates selected fields on an existing Bolna voice AI agent.

```
PUT https://connect.mindcloud.co/v1/universal/bolna/latest/actions/patch-update-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bolna `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bolna/latest/actions/patch-update-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bolna/latest/actions/patch-update-agent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | The ID of the agent. |
| `agentConfig` | object | no | Partial agent configuration payload. |
| `agentPrompts` | object | no | Partial prompt payload keyed by task id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "state": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `state` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bolna API, this operation is `PATCH /v2/agent/:agentId` (base URL `https://api.bolna.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-update-agent.md) for the provider-specific parameters and requirements.

