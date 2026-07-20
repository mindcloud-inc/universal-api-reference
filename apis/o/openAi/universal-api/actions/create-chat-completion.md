# Open AI: Create Chat Completion

Creates a model response for the given chat conversation.

```
POST https://connect.mindcloud.co/v1/universal/openAi/latest/actions/create-chat-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/create-chat-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages[]": [
    {}
  ],
  "messages[].content": "string",
  "messages[].role": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openAi/latest/actions/create-chat-completion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages[]": [{}],
    "messages[].content": "string",
    "messages[].role": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messages[]` | array<object> | yes |  |
| `messages[].content` | string | yes | Accepts multiple values as an array. |
| `messages[].role` | list<string> | yes |  |
| `model` | list<string> | no | Default: `gpt-4o-mini`. |
| `messages[].name` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `responseFormat.type` | list<string> | no | Default: `text`. |
| `frequencyPenalty` | date | no | Number between -2.0 and 2.0. Positive values penalize new tokens based on their existing frequency in the text so far, decreasing the model's likelihood to repeat the same line verbatim. Default: `0`. |
| `presencePenalty` | date | no | Number between -2.0 and 2.0. Positive values penalize new tokens based on whether they appear in the text so far, increasing the model's likelihood to talk about new topics. Default: `0`. |
| `responseFormat` | object | no |  |
| `temperature` | date | no | What sampling temperature to use, between 0 and 2. Higher values like 0.8 will make the output more random, while lower values like 0.2 will make it more focused and deterministic. We generally recommend altering this or top_p but not both. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "choices": [
        {
          "finish_reason": "string",
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
      "usage": {
        "completion_tokens": 1,
        "prompt_tokens": 1,
        "total_tokens": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choices[].finish_reason` | string | Reason generation finished. |
| `choices[].index` | number | Choice index. |
| `choices[].message.content` | string | Generated message text. |
| `choices[].message.role` | string | Role for the returned message. |
| `created` | number | Unix timestamp of creation. |
| `id` | string | The unique identifier for the chat completion. |
| `model` | string | Model used for generation. |
| `object` | string | Object type. |
| `usage.completion_tokens` | number | Output tokens consumed. |
| `usage.prompt_tokens` | number | Input tokens consumed. |
| `usage.total_tokens` | number | Total tokens consumed. |

## Native endpoint

Through the native Open AI API, this operation is `POST v1/chat/completions` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat-completion.md) for the provider-specific parameters and requirements.

