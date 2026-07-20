# Groq: Create Chat Completion

Creates a chat completion in Groq.

```
POST https://connect.mindcloud.co/v1/universal/groq/latest/actions/create-chat-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Groq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/groq/latest/actions/create-chat-completion" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/groq/latest/actions/create-chat-completion', {
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
| `model` | string | yes | The Groq model identifier to use for the chat completion. |
| `messages[]` | array<object> | yes | The chat messages to send, in order. |
| `maxCompletionTokens` | number | no | Upper bound for generated completion tokens. |
| `includeReasoning` | boolean | no |  |
| `reasoningFormat` | list | no |  |
| `citationOptions` | list | no |  |
| `parallelToolCalls` | boolean | no |  |
| `seed` | number | no |  |
| `serviceTier` | list | no |  |
| `topP` | number | no |  |
| `logprobs` | boolean | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `temperature` | number | no | Controls response randomness from 0 to 2. |
| `stream` | boolean | no | When true, return the completion as a stream. |
| `user` | string | no |  |
| `reasoningEffort` | list | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "choices": [
        {
          "finishReason": "string",
          "index": 1,
          "message": {
            "content": "string",
            "role": "string"
          }
        }
      ],
      "created": 1,
      "id": "string",
      "model": "string",
      "object": "string",
      "serviceTier": "string",
      "systemFingerprint": "string",
      "usage": {
        "completionTime": 1,
        "completionTokens": 1,
        "promptTime": 1,
        "promptTokens": 1,
        "queueTime": 1,
        "totalTime": 1,
        "totalTokens": 1
      },
      "xGroq": {
        "id": "string",
        "seed": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choices[].finishReason` | string |  |
| `choices[].index` | number |  |
| `choices[].message.content` | string |  |
| `choices[].message.role` | string |  |
| `created` | number |  |
| `id` | string |  |
| `model` | string |  |
| `object` | string |  |
| `serviceTier` | string |  |
| `systemFingerprint` | string |  |
| `usage.completionTime` | number |  |
| `usage.completionTokens` | number |  |
| `usage.promptTime` | number |  |
| `usage.promptTokens` | number |  |
| `usage.queueTime` | number |  |
| `usage.totalTime` | number |  |
| `usage.totalTokens` | number |  |
| `xGroq.id` | string |  |
| `xGroq.seed` | number |  |

## Native endpoint

Through the native Groq API, this operation is `POST /openai/v1/chat/completions` (base URL `https://api.groq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat-completion.md) for the provider-specific parameters and requirements.

