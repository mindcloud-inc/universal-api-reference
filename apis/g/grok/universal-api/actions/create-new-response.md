# Grok: Create New Response

Creates a new response in Grok.

```
POST https://connect.mindcloud.co/v1/universal/grok/latest/actions/create-new-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grok/latest/actions/create-new-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grok/latest/actions/create-new-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | no | Model ID to use for the response. |
| `input` | string | yes | Text or structured input for the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": 1,
      "createdAt": 1,
      "id": "string",
      "model": "string",
      "object": "string",
      "output": [
        {
          "content": [
            {
              "text": "string",
              "type": "string"
            }
          ],
          "id": "string",
          "role": "string",
          "status": "string",
          "type": "string"
        }
      ],
      "parallelToolCalls": true,
      "status": "string",
      "temperature": 1,
      "toolChoice": "string",
      "topP": 1,
      "usage": {
        "inputTokens": 1,
        "inputTokensDetails": {
          "cachedTokens": 1
        },
        "outputTokens": 1,
        "outputTokensDetails": {
          "reasoningTokens": 1
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
| `completedAt` | number | Unix timestamp when the response completed. |
| `createdAt` | number | Unix timestamp when the response was created. |
| `id` | string | Response identifier. |
| `model` | string | Model used to generate the response. |
| `object` | string | Provider object type. |
| `output` | array<object> | Generated output items returned by xAI. |
| `output[].content` | array<object> | Content blocks for the output item. |
| `output[].content[].text` | string | Rendered text for the content block. |
| `output[].content[].type` | string | Content block type. |
| `output[].id` | string | Message item identifier. |
| `output[].role` | string | Role for the output item. |
| `output[].status` | string | Completion status for the output item. |
| `output[].type` | string | Output item type. |
| `parallelToolCalls` | boolean | Whether parallel tool calling was enabled. |
| `status` | string | Lifecycle status of the response. |
| `temperature` | number | Sampling temperature used for the response. |
| `toolChoice` | string | Tool selection mode used by the response. |
| `topP` | number | Top-p sampling value used for the response. |
| `usage` | object | Token usage metadata for the response. |
| `usage.inputTokens` | number | Input token count. |
| `usage.inputTokensDetails` | object | Detailed input token usage. |
| `usage.inputTokensDetails.cachedTokens` | number | Cached input token count. |
| `usage.outputTokens` | number | Output token count. |
| `usage.outputTokensDetails` | object | Detailed output token usage. |
| `usage.outputTokensDetails.reasoningTokens` | number | Reasoning token count. |
| `usage.totalTokens` | number | Total token count. |

## Native endpoint

Through the native Grok API, this operation is `POST /v1/responses` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-new-response.md) for the provider-specific parameters and requirements.

