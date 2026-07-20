# DeepSeek: Create Chat Prefix Completion (Beta)



```
POST https://connect.mindcloud.co/v1/universal/deepSeek/latest/actions/create-chat-prefix-completion-beta
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepSeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepSeek/latest/actions/create-chat-prefix-completion-beta" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "deepseek-chat",
  "messages[]": "[object Object],[object Object]",
  "messages[].role": "assistant",
  "messages[].content": "string",
  "tools[].type": "function",
  "tools[].function": {},
  "tools[].function.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepSeek/latest/actions/create-chat-prefix-completion-beta', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "deepseek-chat",
    "messages[]": "[object Object],[object Object]",
    "messages[].role": "assistant",
    "messages[].content": "string",
    "tools[].type": "function",
    "tools[].function": {},
    "tools[].function.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | list | yes | Model ID to use One of: `deepseek-chat`, `deepseek-reasoner`. Default: `deepseek-chat`. |
| `messages[]` | array | yes | Conversation messages; last message must be assistant with prefix=true Example: `[object Object],[object Object]`. |
| `temperature` | number | no | Sampling temperature (0-2) Default: `1`. |
| `max_tokens` | number | no | Maximum tokens to generate Default: `4096`. |
| `top_p` | number | no | Nucleus sampling (0-1) Default: `1`. |
| `stop[]` | array<string> | no | Stop sequences |
| `stream` | boolean | no | Enable streaming response Default: `false`. |
| `streamOptionsIncludeUsage` | boolean | no | Include usage chunk when stream=true Default: `false`. |
| `logprobs` | boolean | no | Whether to return log probabilities Default: `false`. |
| `response_format.type` | list | no | Response format type One of: `json_object`, `text`. Default: `text`. |
| `frequency_penalty` | number | no | Penalize repeated tokens (-2 to 2) Default: `0`. |
| `presence_penalty` | number | no | Penalize tokens already in text (-2 to 2) Default: `0`. |
| `thinkingType` | list | no | Reasoning mode type One of: `disabled`, `enabled`. |
| `tools[]` | array<object> | no | JSON array of tool/function definitions for function calling |
| `tool_choice` | string | no | Tool choice mode or JSON object Default: `auto`. |
| `top_logprobs` | number | no | Number of most likely tokens to return (requires logprobs=true) |
| `messages[].role` | list | yes | Role of each message One of: `assistant`, `system`, `tool`, `user`. |
| `messages[].content` | string | yes | Content of each message |
| `messages[].name` | string | no | Optional participant name |
| `messages[].tool_call_id` | string | no | Tool call ID for tool-role messages |
| `messages[].prefix` | boolean | no | Enable prefix completion on assistant message Default: `false`. |
| `tools[].type` | list | yes | Tool type One of: `function`. |
| `tools[].function` | object | yes | Function definition object |
| `tools[].function.name` | string | yes | Function name |
| `tools[].function.description` | string | no | Function description |
| `tools[].function.parameters` | object | no | JSON Schema describing function parameters |
| `tools[].function.strict` | boolean | no | Enable strict schema adherence Default: `false`. |
| `response_format` | object | no | Response format object |

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
            "reasoningContent": "string",
            "role": "string",
            "toolCalls": [
              {
                "function": {
                  "arguments": "string",
                  "name": "Ava Chen"
                },
                "id": "string",
                "type": "string"
              }
            ]
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
        "promptCacheHitTokens": 1,
        "promptCacheMissTokens": 1,
        "promptTokens": 1,
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
| `choices[].finishReason` | string |  |
| `choices[].index` | number |  |
| `choices[].message.content` | string |  |
| `choices[].message.reasoningContent` | string |  |
| `choices[].message.role` | string |  |
| `choices[].message.toolCalls[].function.arguments` | string |  |
| `choices[].message.toolCalls[].function.name` | string |  |
| `choices[].message.toolCalls[].id` | string |  |
| `choices[].message.toolCalls[].type` | string |  |
| `created` | number |  |
| `id` | string |  |
| `model` | string |  |
| `object` | string |  |
| `systemFingerprint` | string |  |
| `usage.completionTokens` | number |  |
| `usage.completionTokensDetails.reasoningTokens` | number |  |
| `usage.promptCacheHitTokens` | number |  |
| `usage.promptCacheMissTokens` | number |  |
| `usage.promptTokens` | number |  |
| `usage.totalTokens` | number |  |

## Native endpoint

Through the native DeepSeek API, this operation is `POST /beta/chat/completions` (base URL `https://api.deepseek.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat-prefix-completion-beta.md) for the provider-specific parameters and requirements.

