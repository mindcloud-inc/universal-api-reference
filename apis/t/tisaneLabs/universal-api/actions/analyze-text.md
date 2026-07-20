# Tisane Labs: Analyze Text

Analyzes input text in Tisane Labs.

```
GET https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/analyze-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tisane Labs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/analyze-text?connectionId=$CONNECTION_ID&language=en&content=Hello%20Tisane%20API!" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "language": "en",
  "content": "Hello Tisane API!"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/analyze-text?${params}`, {
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
| `language` | string | yes | Language code for the text to analyze. Example: `en`. |
| `content` | string | yes | Text content to analyze. Example: `Hello Tisane API!`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `settings` | object | no | Optional Tisane analysis settings object. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abuse": [
        {}
      ],
      "entities_summary": [
        {}
      ],
      "language": "string",
      "memory": {},
      "sentence_list": [
        {}
      ],
      "sentiment_expressions": [
        {}
      ],
      "text": "string",
      "topics": [
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
| `abuse` | array<object> | Problematic content snippets. |
| `entities_summary` | array<object> | Detected named entities. |
| `language` | string | Detected or specified language code. |
| `memory` | object | Analysis state when requested. |
| `sentence_list` | array<object> | Sentence, word, and parse details when requested. |
| `sentiment_expressions` | array<object> | Detected sentiment snippets. |
| `text` | string | Input text. |
| `topics` | array<string> | Detected topics. |

## Native endpoint

Through the native Tisane Labs API, this operation is `POST /parse` (base URL `https://api.tisane.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-text.md) for the provider-specific parameters and requirements.

