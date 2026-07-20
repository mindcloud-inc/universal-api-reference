# Sapling: Detect AI-Generated Text

Detects whether text is AI-generated with Sapling.

```
GET https://connect.mindcloud.co/v1/universal/sapling/latest/actions/detect-ai-generated-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sapling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sapling/latest/actions/detect-ai-generated-text?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sapling/latest/actions/detect-ai-generated-text?${params}`, {
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
| `text` | string | yes | Text to run AI detection on. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "score": 1,
      "sentence_scores": [
        {}
      ],
      "text": "string",
      "token_probs": [
        1
      ],
      "tokens": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `score` | number | Overall AI-generation probability score. |
| `sentence_scores` | array<object> | Per-sentence AI-generation scores. |
| `text` | string | Analyzed input text. |
| `token_probs` | array<number> | Per-token probabilities. |
| `tokens` | array<string> | Tokenized input text. |

## Native endpoint

Through the native Sapling API, this operation is `POST /api/v1/aidetect` (base URL `https://api.sapling.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-ai-generated-text.md) for the provider-specific parameters and requirements.

