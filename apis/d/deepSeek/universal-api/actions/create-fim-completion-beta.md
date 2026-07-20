# DeepSeek: Create FIM Completion (Beta)



```
POST https://connect.mindcloud.co/v1/universal/deepSeek/latest/actions/create-fim-completion-beta
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepSeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepSeek/latest/actions/create-fim-completion-beta" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "def fibonacci(n):"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepSeek/latest/actions/create-fim-completion-beta', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "def fibonacci(n):"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | yes | The prefix text to complete Example: `def fibonacci(n):`. |
| `suffix` | string | no | Text that comes after the completion Example: `return result`. |
| `max_tokens` | number | no | Maximum tokens to generate Default: `4096`. |
| `temperature` | number | no | Sampling temperature (0-2) Default: `1`. |
| `top_p` | number | no | Nucleus sampling (0-1) Default: `1`. |
| `frequency_penalty` | number | no | Penalize repeated tokens (-2 to 2) Default: `0`. |
| `presence_penalty` | number | no | Penalize tokens already present (-2 to 2) Default: `0`. |
| `logprobs` | number | no | Number of top log probabilities to return |
| `stop[]` | array<string> | no | Stop sequences |
| `stream` | boolean | no | Enable streaming response Default: `false`. |
| `streamOptionsIncludeUsage` | boolean | no | Include usage chunk when stream=true Default: `false`. |
| `echo` | boolean | no | Echo back the prompt in the completion response Default: `false`. |

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
          "logprobs": {
            "textOffset": [
              1
            ],
            "tokenLogprobs": [
              1
            ],
            "tokens": [
              "string"
            ]
          },
          "text": "string"
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
| `choices[].logprobs.textOffset[]` | number |  |
| `choices[].logprobs.tokenLogprobs[]` | number |  |
| `choices[].logprobs.tokens[]` | string |  |
| `choices[].text` | string |  |
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

Through the native DeepSeek API, this operation is `POST /beta/completions` (base URL `https://api.deepseek.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-fim-completion-beta.md) for the provider-specific parameters and requirements.

