# Ollama: Generate Response

Generates a response from an Ollama model.

```
POST https://connect.mindcloud.co/v1/universal/ollama/latest/actions/generate-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ollama `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ollama/latest/actions/generate-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ollama/latest/actions/generate-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes |  |
| `prompt` | string | yes |  |
| `suffix` | string | no | Text that appears after the prompt for fill-in-the-middle generation. |
| `images[]` | array<string> | no | Base64-encoded images for models that support image input. |
| `format` | string | no | Use json or provide a JSON schema object for structured output. |
| `system` | string | no |  |
| `options` | object | no |  |
| `stream` | boolean | no |  |
| `think` | string | no | Use true or false, or high/medium/low for supported models. |
| `raw` | boolean | no |  |
| `keepAlive` | string | no |  |
| `logprobs` | boolean | no |  |
| `topLogprobs` | number | no |  |

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
      "model": "string",
      "promptEvalCount": 1,
      "promptEvalDuration": 1,
      "response": "string",
      "thinking": "string",
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
| `model` | string |  |
| `promptEvalCount` | number |  |
| `promptEvalDuration` | number |  |
| `response` | string |  |
| `thinking` | string |  |
| `totalDuration` | number |  |

## Native endpoint

Through the native Ollama API, this operation is `POST /api/generate` (base URL `https://ollama.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-response.md) for the provider-specific parameters and requirements.

