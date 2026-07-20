# Bolna: Create Agent

Creates a new voice AI agent in Bolna.

```
POST https://connect.mindcloud.co/v1/universal/bolna/latest/actions/create-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bolna `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bolna/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentConfig": {},
  "agentPrompts": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bolna/latest/actions/create-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `agentConfig` | object | yes | Configuration payload for the agent. |
| `agentPrompts` | object | yes | Prompt payload keyed by task id. |

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

Through the native Bolna API, this operation is `POST /v2/agent` (base URL `https://api.bolna.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent.md) for the provider-specific parameters and requirements.

