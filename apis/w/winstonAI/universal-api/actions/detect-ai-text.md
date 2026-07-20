# Winston AI: Detect AI Text



```
GET https://connect.mindcloud.co/v1/universal/winstonAI/latest/actions/detect-ai-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Winston AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/winstonAI/latest/actions/detect-ai-text?connectionId=$CONNECTION_ID&text=Paste%20at%20least%20300%20characters%20of%20text%20to%20scan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "Paste at least 300 characters of text to scan"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/winstonAI/latest/actions/detect-ai-text?${params}`, {
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
| `text` | string | yes | The text to scan for AI-generated content. Example: `Paste at least 300 characters of text to scan`. |
| `version` | string | no | The Winston AI model version to use. Example: `latest`. |
| `sentences` | boolean | no | Include per-sentence scores in the response. Default: `true`. |
| `language` | string | no | Two-letter language code, or auto for auto-detection. Default: `auto`. Example: `auto`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | string | no | A public PDF, DOC, or DOCX URL to scan instead of raw text. Example: `https://example.com/file.pdf`. |
| `website` | string | no | A public website URL to scan instead of raw text. Example: `https://example.com/article`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attack_detected": {},
      "credits_remaining": 1,
      "credits_used": 1,
      "input": "string",
      "language": "string",
      "length": 1,
      "readability_score": 1,
      "score": 1,
      "sentences": [
        {}
      ],
      "status": 1,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attack_detected` | object | Indicators for zero-width-space and homoglyph attacks. |
| `credits_remaining` | number | Remaining Winston AI credits after the scan. |
| `credits_used` | number | Credits consumed by the scan. |
| `input` | string | Input mode used by the scan, such as text, file, or website. |
| `language` | string | Detected language code. |
| `length` | number | Length of the processed input text. |
| `readability_score` | number | Readability score for the processed text. |
| `score` | number | Human-written score returned by Winston AI. |
| `sentences` | array<object> | Per-sentence scoring details when sentence output is enabled. |
| `status` | number | HTTP status code returned by Winston AI. |
| `version` | string | Model version used for the prediction. |

## Native endpoint

Through the native Winston AI API, this operation is `POST /v2/ai-content-detection` (base URL `https://api.gowinston.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-ai-text.md) for the provider-specific parameters and requirements.

