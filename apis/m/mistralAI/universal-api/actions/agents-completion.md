# Mistral AI: Agents Completion

Creates an agent completion in Mistral AI.

```
POST https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/agents-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mistral AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/agents-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "messages[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/agents-completion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "messages[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | The ID of the agent to use for this completion. |
| `messages[]` | array<object> | yes | Prompt messages encoded as a list of role/content objects. |
| `maxTokens` | number | no | Maximum number of tokens to generate. |
| `stream` | boolean | no | Whether to stream partial progress. |
| `stop` | string | no | Stop generation when a token or one of the provided tokens is detected. |
| `randomSeed` | number | no | Seed to use for deterministic random sampling. |
| `promptMode` | string | no | Prompt behavior mode such as reasoning. |
| `responseFormat` | object | no | Structured output format settings. |
| `tools[]` | array<object> | no | Tool definitions available to the agent. |
| `toolChoice` | string | no | Tool selection behavior for the completion. |
| `parallelToolCalls` | boolean | no | Allow the agent to call tools in parallel. |
| `metadata` | object | no | Optional metadata object for the request. |
| `prediction` | object | no | Expected completion content for response-time optimization. |
| `presencePenalty` | number | no | Penalty that encourages topic diversity. |
| `frequencyPenalty` | number | no | Penalty that discourages repetition. |
| `n` | number | no | Number of completions to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "choices": [
        {}
      ],
      "created": 1,
      "id": "string",
      "model": "string",
      "object": "string",
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choices` | array<object> |  |
| `created` | number |  |
| `id` | string |  |
| `model` | string |  |
| `object` | string |  |
| `usage` | object |  |

## Native endpoint

Through the native Mistral AI API, this operation is `POST /v1/agents/completions` (base URL `https://api.mistral.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/agents-completion.md) for the provider-specific parameters and requirements.

