# Letta: Create Agent Message

Processes a user message through an agent in Letta.

```
POST https://connect.mindcloud.co/v1/universal/letta/latest/actions/create-agent-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Letta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/letta/latest/actions/create-agent-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "input": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/letta/latest/actions/create-agent-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "input": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | The Letta agent ID. |
| `input` | string | yes | The user message to send to the agent. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messages": [
        {}
      ],
      "stop_reason": {},
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messages` | array<object> |  |
| `stop_reason` | object |  |
| `usage` | object |  |

## Native endpoint

Through the native Letta API, this operation is `POST /v1/agents/:agent_id/messages` (base URL `https://api.letta.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent-message.md) for the provider-specific parameters and requirements.

