# LLMLayer: Answer with Domain Filter

Retrieves a domain-filtered answer from LLMLayer.

```
GET https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/answer-with-domain-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LLMLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/answer-with-domain-filter?connectionId=$CONNECTION_ID&query=Ask%20a%20question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "Ask a question"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/answer-with-domain-filter?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | Question or prompt to answer with domain filters. Example: `Ask a question`. |
| `domainFilter[]` | array<string> | no | Include or exclude domains from the answer context. Example: `example.com,-reddit.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "images": [
        {}
      ],
      "input_tokens": 1,
      "llmlayer_cost": 1,
      "model_cost": 1,
      "output_tokens": 1,
      "response_time": "string",
      "sources": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string | AI-generated answer text. |
| `images` | array<object> | Related images returned by LLMLayer. |
| `input_tokens` | number | Input token count. |
| `llmlayer_cost` | number | LLMLayer request cost. |
| `model_cost` | number | Underlying model cost. |
| `output_tokens` | number | Output token count. |
| `response_time` | string | Server-side response time. |
| `sources` | array<object> | Supporting sources returned by LLMLayer. |

## Native endpoint

Through the native LLMLayer API, this operation is `POST /api/v2/answer` (base URL `https://api.llmlayer.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/answer-with-domain-filter.md) for the provider-specific parameters and requirements.

