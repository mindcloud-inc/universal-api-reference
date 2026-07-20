# Winston AI: Check Facts



```
GET https://connect.mindcloud.co/v1/universal/winstonAI/latest/actions/check-facts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Winston AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/winstonAI/latest/actions/check-facts?connectionId=$CONNECTION_ID&text=Paste%20at%20least%20300%20characters%20of%20text%20to%20fact-check" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "Paste at least 300 characters of text to fact-check"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/winstonAI/latest/actions/check-facts?${params}`, {
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
| `text` | string | yes | The text to fact-check. Example: `Paste at least 300 characters of text to fact-check`. |
| `language` | string | no | Two-letter language code, or auto for auto-detection. Default: `auto`. Example: `auto`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | string | no | A public PDF, DOC, or DOCX URL to fact-check instead of raw text. Example: `https://example.com/file.pdf`. |
| `website` | string | no | A public website URL to fact-check instead of raw text. Example: `https://example.com/article`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "claims": [
        {}
      ],
      "claimsCount": 1,
      "creditsRemaining": 1,
      "creditsUsed": 1,
      "input": "string",
      "language": "string",
      "score": 1,
      "sentences": [
        {}
      ],
      "status": 1,
      "text": "string",
      "wordCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `claims` | array<object> | Extracted claims and their fact-check results. |
| `claimsCount` | number | Number of claims extracted from the text. |
| `creditsRemaining` | number | Remaining Winston AI credits after the request. |
| `creditsUsed` | number | Credits consumed by the fact-check request. |
| `input` | string | Input mode used by the request. |
| `language` | string | Detected or specified language code. |
| `score` | number | Overall factual-accuracy score for the input text. |
| `sentences` | array<object> | Sentences extracted from the analyzed text. |
| `status` | number | HTTP status code returned by Winston AI. |
| `text` | string | Original text analyzed by the fact checker. |
| `wordCount` | number | Word count of the analyzed input. |

## Native endpoint

Through the native Winston AI API, this operation is `POST /v2/fact-checker` (base URL `https://api.gowinston.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-facts.md) for the provider-specific parameters and requirements.

