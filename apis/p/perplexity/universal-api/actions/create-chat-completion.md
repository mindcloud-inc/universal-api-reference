# Perplexity: Create Chat Completion

Creates a chat completion in Perplexity.

```
POST https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/create-chat-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perplexity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/create-chat-completion" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/create-chat-completion', {
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
| `model` | string | yes | Sonar model to use, for example sonar-pro. |
| `messages[]` | array<object> | yes | Conversation history array in OpenAI chat format. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `maxTokens` | number | no | Maximum number of completion tokens to generate. |
| `stream` | boolean | no | When true, returns a streaming SSE response. |
| `temperature` | number | no | Controls randomness in the response. |
| `disableSearch` | boolean | no | When true, disables web search for this request. |
| `searchDomainFilter[]` | array<string> | no | Limit search results to specific domains. |
| `searchLanguageFilter[]` | array<string> | no | Filter search results by ISO 639-1 language code. |
| `searchRecencyFilter` | string | no | Filter by publication recency. |
| `reasoningEffort` | string | no | Controls how much effort the model spends on reasoning. |
| `languagePreference` | string | no | ISO 639-1 language code for the preferred response language. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "choices": [
        {
          "finish_reason": "string",
          "message": {
            "content": "string",
            "role": "string"
          }
        }
      ],
      "citations": [
        [
          "string"
        ]
      ],
      "created": 1,
      "id": "string",
      "model": "string",
      "object": "string",
      "related_questions": [
        [
          "string"
        ]
      ],
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
| `choices[].finish_reason` | string |  |
| `choices[].message.content` | string |  |
| `choices[].message.role` | string |  |
| `citations[]` | array<string> |  |
| `created` | number |  |
| `id` | string |  |
| `model` | string |  |
| `object` | string |  |
| `related_questions[]` | array<string> |  |
| `usage.completion_tokens` | number |  |
| `usage.prompt_tokens` | number |  |
| `usage.total_tokens` | number |  |

## Native endpoint

Through the native Perplexity API, this operation is `POST /v1/sonar` (base URL `https://api.perplexity.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat-completion.md) for the provider-specific parameters and requirements.

