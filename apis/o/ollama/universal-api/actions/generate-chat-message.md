# Ollama: Generate Chat Message

Generates the next chat message in Ollama.

```
POST https://connect.mindcloud.co/v1/universal/ollama/latest/actions/generate-chat-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ollama `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ollama/latest/actions/generate-chat-message" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/ollama/latest/actions/generate-chat-message', {
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
| `tools[]` | array<object> | no | Function tools the model may call during chat. |
| `format` | string | no | Use json or provide a JSON schema object for structured output. |
| `options` | object | no |  |
| `stream` | boolean | no |  |
| `think` | string | no | Use true or false, or high/medium/low for supported models. |
| `keepAlive` | string | no |  |
| `logprobs` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "done": true,
      "doneReason": "string",
      "evalCount": 1,
      "evalDuration": 1,
      "loadDuration": 1,
      "logprobs": [
        {}
      ],
      "message": {},
      "model": "string",
      "promptEvalCount": 1,
      "promptEvalDuration": 1,
      "totalDuration": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `done` | boolean |  |
| `doneReason` | string |  |
| `evalCount` | number |  |
| `evalDuration` | number |  |
| `loadDuration` | number |  |
| `logprobs` | array<object> |  |
| `message` | object |  |
| `model` | string |  |
| `promptEvalCount` | number |  |
| `promptEvalDuration` | number |  |
| `totalDuration` | number |  |

## Native endpoint

Through the native Ollama API, this operation is `POST /api/chat` (base URL `https://ollama.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-chat-message.md) for the provider-specific parameters and requirements.

