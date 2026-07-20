# Mistral AI: Chat Completion

Creates a chat completion in Mistral AI.

```
POST https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/chat-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mistral AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/chat-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "messages[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/chat-completion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "messages[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes |  |
| `messages[]` | array<object> | yes | Conversation messages array |
| `temperature` | number | no |  |
| `topP` | number | no |  |
| `maxTokens` | number | no |  |
| `stream` | boolean | no |  |
| `stop` | string | no |  |
| `randomSeed` | number | no |  |
| `safePrompt` | boolean | no |  |
| `promptMode` | string | no |  |
| `responseFormat` | object | no | Structured output format settings |
| `tools[]` | array<object> | no | Tool definitions available to the model |
| `toolChoice` | string | no |  |
| `parallelToolCalls` | boolean | no |  |
| `guardrails[]` | array<object> | no | Guardrail configuration list |
| `metadata` | object | no |  |
| `prediction` | object | no |  |
| `presencePenalty` | number | no |  |
| `frequencyPenalty` | number | no |  |
| `n` | number | no |  |

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

Through the native Mistral AI API, this operation is `POST /v1/chat/completions` (base URL `https://api.mistral.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/chat-completion.md) for the provider-specific parameters and requirements.

