# Letta: Create Agent

Creates a new agent in Letta.

```
POST https://connect.mindcloud.co/v1/universal/letta/latest/actions/create-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Letta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/letta/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/letta/latest/actions/create-agent', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | no | Model handle to use for the new Letta agent, such as openai/gpt-4.1. |
| `name` | string | no | Optional display name for the agent. |
| `blockIds[]` | array<string> | no | Optional Letta block IDs to attach to the agent when it is created. |
| `memoryBlocks[]` | array<object> | no | Optional memory blocks to create in the agent's in-context memory. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent_type": "string",
      "id": "string",
      "model": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent_type` | string |  |
| `id` | string |  |
| `model` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Letta API, this operation is `POST /v1/agents/` (base URL `https://api.letta.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent.md) for the provider-specific parameters and requirements.

