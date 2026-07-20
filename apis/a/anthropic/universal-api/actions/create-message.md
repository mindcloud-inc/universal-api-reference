# Anthropic: Create Message

Creates the next message in an Anthropic conversation.

```
POST https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/create-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/create-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "claude-sonnet-4-5-20250929",
  "maxTokens": "1024",
  "messages[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/create-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "claude-sonnet-4-5-20250929",
    "maxTokens": "1024",
    "messages[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | The model that will complete your prompt. Example: `claude-sonnet-4-5-20250929`. |
| `maxTokens` | number | yes | The maximum number of tokens to generate before stopping. Example: `1024`. |
| `messages[]` | array<object> | yes | Input conversation messages. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `temperature` | number | no | Amount of randomness injected into responses. Example: `0.7`. |
| `topP` | number | no | Nucleus sampling parameter. Example: `0.9`. |
| `topK` | number | no | Only sample from the top K options. Example: `40`. |
| `stream` | boolean | no | Whether to stream response chunks. |
| `stopSequences[]` | array<string> | no | Custom sequences that stop generation. |

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
      "stopSequence": "string",
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
| `stopSequence` | string |  |
| `type` | string |  |
| `usage` | object |  |

## Native endpoint

Through the native Anthropic API, this operation is `POST /v1/messages` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-message.md) for the provider-specific parameters and requirements.

