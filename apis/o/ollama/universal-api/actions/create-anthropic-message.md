# Ollama: Create Anthropic Message

Creates an Anthropic-compatible message in Ollama.

```
POST https://connect.mindcloud.co/v1/universal/ollama/latest/actions/create-anthropic-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ollama `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ollama/latest/actions/create-anthropic-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "maxTokens": 1,
  "messages[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ollama/latest/actions/create-anthropic-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "maxTokens": 1,
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
| `maxTokens` | number | yes |  |
| `messages[]` | array<object> | yes | Array of message objects. |
| `system` | string | no |  |
| `stream` | boolean | no |  |
| `temperature` | number | no |  |
| `topP` | number | no |  |
| `topK` | number | no |  |
| `stopSequences[]` | array<string> | no |  |
| `tools[]` | array<object> | no |  |
| `thinking` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        {}
      ],
      "id": "string",
      "model": "string",
      "role": "string",
      "stopReason": "string",
      "type": "string",
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | array<object> |  |
| `id` | string |  |
| `model` | string |  |
| `role` | string |  |
| `stopReason` | string |  |
| `type` | string |  |
| `usage` | object |  |

## Native endpoint

Through the native Ollama API, this operation is `POST /v1/messages` (base URL `https://ollama.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-anthropic-message.md) for the provider-specific parameters and requirements.

