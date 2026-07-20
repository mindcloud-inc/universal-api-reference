# Bolna: Update Agent

Updates an existing voice AI agent in Bolna.

```
PUT https://connect.mindcloud.co/v1/universal/bolna/latest/actions/update-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bolna `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bolna/latest/actions/update-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "agentConfig": {},
  "agentPrompts": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bolna/latest/actions/update-agent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "agentConfig": {},
    "agentPrompts": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | The ID of the agent. |
| `agentConfig` | object | yes | Full replacement configuration payload for the agent. |
| `agentPrompts` | object | yes | Full replacement prompt payload keyed by task id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string |  |
| `state` | string |  |

## Native endpoint

Through the native Bolna API, this operation is `PUT /v2/agent/:agentId` (base URL `https://api.bolna.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-agent.md) for the provider-specific parameters and requirements.

