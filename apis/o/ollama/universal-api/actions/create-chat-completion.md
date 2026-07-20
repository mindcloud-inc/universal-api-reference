# Ollama: Create Chat Completion

Creates an OpenAI-compatible chat completion in Ollama.

```
POST https://connect.mindcloud.co/v1/universal/ollama/latest/actions/create-chat-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ollama `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ollama/latest/actions/create-chat-completion" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/ollama/latest/actions/create-chat-completion', {
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
| `messages[]` | array<object> | yes | Array of chat message objects. |
| `temperature` | number | no |  |
| `maxTokens` | number | no |  |
| `topP` | number | no |  |
| `frequencyPenalty` | number | no |  |
| `presencePenalty` | number | no |  |
| `responseFormat` | object | no |  |
| `stream` | boolean | no |  |
| `streamOptions` | object | no |  |
| `stop[]` | array<string> | no |  |
| `tools[]` | array<object> | no |  |
| `toolChoice` | string | no |  |
| `reasoningEffort` | string | no |  |
| `reasoning` | object | no |  |
| `logitBias` | object | no |  |
| `user` | string | no |  |
| `n` | number | no |  |
| `seed` | number | no |  |

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

Through the native Ollama API, this operation is `POST /v1/chat/completions` (base URL `https://ollama.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat-completion.md) for the provider-specific parameters and requirements.

