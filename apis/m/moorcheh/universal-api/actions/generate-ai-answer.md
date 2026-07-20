# Moorcheh: Generate AI Answer

Generates an AI answer in Moorcheh from your data.

```
POST https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/generate-ai-answer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moorcheh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/generate-ai-answer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "namespace": "Ava Chen",
  "query": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/generate-ai-answer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "namespace": "Ava Chen",
    "query": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `namespace` | string | yes | Namespace for search mode, or an empty string for direct AI mode. |
| `query` | string | yes | Question or prompt to answer. |
| `top_k` | number | no | Number of relevant chunks to use in search mode. Defaults to 10 in Moorcheh. Default: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threshold` | number | no | Minimum relevance score from 0 to 1. Required when kiosk mode is enabled. |
| `temperature` | number | no | AI creativity level from 0.0 to 2.0. Moorcheh defaults to 0.7. Default: `0.7`. |
| `ai_model` | string | no | Optional Moorcheh AI model ID such as deepseek.r1-v1:0. |
| `kiosk_mode` | boolean | no | Enable threshold-based filtering for namespace-backed answers. |
| `header_prompt` | string | no | Optional instruction prepended to the model prompt. |
| `footer_prompt` | string | no | Optional instruction appended to the prompt. Moorcheh defaults to a concise-answer instruction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "context_count": 1,
      "model": "string",
      "query": "string",
      "structured_data": {},
      "used_context": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string | Generated answer. |
| `context_count` | number | Number of context chunks used. |
| `model` | string | AI model used by Moorcheh. |
| `query` | string | Original query. |
| `structured_data` | object | Structured response object when requested. |
| `used_context` | boolean | Whether namespace context was used. |

## Native endpoint

Through the native Moorcheh API, this operation is `POST /answer` (base URL `https://api.moorcheh.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-ai-answer.md) for the provider-specific parameters and requirements.

