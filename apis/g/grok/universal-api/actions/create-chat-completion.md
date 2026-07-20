# Grok: Create Chat Completion

Creates a chat completion in Grok.

```
POST https://connect.mindcloud.co/v1/universal/grok/latest/actions/create-chat-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grok/latest/actions/create-chat-completion" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/grok/latest/actions/create-chat-completion', {
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
| `model` | string | yes | Model ID to use for the chat completion. |
| `messages[]` | array<object> | yes |  |

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
      "systemFingerprint": "string",
      "usage": {
        "completionTokens": 1,
        "completionTokensDetails": {
          "reasoningTokens": 1
        },
        "promptTokens": 1,
        "promptTokensDetails": {
          "cachedTokens": 1
        },
        "totalTokens": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choices` | array<object> | Completion choices returned by xAI. |
| `choices[].finishReason` | string | Reason the choice finished. |
| `choices[].index` | number | Choice index. |
| `choices[].message` | object | Assistant message for the choice. |
| `choices[].message.content` | string | Text content for the returned message. |
| `choices[].message.role` | string | Role for the returned message. |
| `created` | number | Unix timestamp when the completion was created. |
| `id` | string | Chat completion identifier. |
| `model` | string | Model used to generate the completion. |
| `object` | string | Provider object type. |
| `systemFingerprint` | string | Provider fingerprint for the serving system. |
| `usage` | object | Token usage metadata for the completion. |
| `usage.completionTokens` | number | Completion token count. |
| `usage.completionTokensDetails` | object | Detailed completion token usage. |
| `usage.completionTokensDetails.reasoningTokens` | number | Reasoning token count. |
| `usage.promptTokens` | number | Prompt token count. |
| `usage.promptTokensDetails` | object | Detailed prompt token usage. |
| `usage.promptTokensDetails.cachedTokens` | number | Cached prompt token count. |
| `usage.totalTokens` | number | Total token count. |

## Native endpoint

Through the native Grok API, this operation is `POST /v1/chat/completions` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat-completion.md) for the provider-specific parameters and requirements.

