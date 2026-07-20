# Agent.ai: Invoke Agent

Invokes an agent in Agent.ai with input or a prompt.

```
POST https://connect.mindcloud.co/v1/universal/agentai/latest/actions/invoke-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/invoke-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "userInput": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentai/latest/actions/invoke-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "userInput": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Agent ID or human-readable slug. |
| `userInput` | string | yes | Prompt or input text for the agent. |
| `runId` | string | no | Optional run identifier for resuming a knowledge-agent conversation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string",
      "run_id": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Agent response text. |
| `run_id` | string | Run identifier for resuming a knowledge-agent conversation. |
| `status` | number | HTTP status code of the action response. |

## Native endpoint

Through the native Agent.ai API, this operation is `POST /action/invoke_agent` (base URL `https://api-lr.agent.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invoke-agent.md) for the provider-specific parameters and requirements.

