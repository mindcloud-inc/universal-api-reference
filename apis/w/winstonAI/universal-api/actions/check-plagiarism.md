# Winston AI: Check Plagiarism



```
GET https://connect.mindcloud.co/v1/universal/winstonAI/latest/actions/check-plagiarism
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Winston AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/winstonAI/latest/actions/check-plagiarism?connectionId=$CONNECTION_ID&text=Paste%20at%20least%20100%20characters%20of%20text%20to%20scan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "Paste at least 100 characters of text to scan"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/winstonAI/latest/actions/check-plagiarism?${params}`, {
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
| `text` | string | yes | The text to scan for plagiarism. Example: `Paste at least 100 characters of text to scan`. |
| `language` | string | no | Two-letter language code, or auto for auto-detection. Default: `auto`. Example: `auto`. |
| `country` | string | no | Country code to guide the scan context. Default: `us`. Example: `us`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | string | no | A public PDF, DOC, or DOCX URL to scan instead of raw text. Example: `https://example.com/file.pdf`. |
| `website` | string | no | A public website URL to scan instead of raw text. Example: `https://example.com/article`. |
| `excludedSources[]` | array<string> | no | Domains or URLs to exclude from the plagiarism score. Example: `example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attackDetected": {},
      "citations": [
        "string"
      ],
      "credits_remaining": 1,
      "credits_used": 1,
      "indexes": [
        {}
      ],
      "result": {},
      "scanInformation": {},
      "similarWords": [
        {}
      ],
      "sources": [
        {}
      ],
      "status": 1,
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attackDetected` | object | Indicators for zero-width-space and homoglyph attacks. |
| `citations` | array<string> | Detected citations in the provided text. |
| `credits_remaining` | number | Remaining Winston AI credits after the scan. |
| `credits_used` | number | Credits consumed by the scan. |
| `indexes` | array<object> | Plagiarism sequence ranges found in the input text. |
| `result` | object | Overall plagiarism scan summary metrics. |
| `scanInformation` | object | Metadata about the plagiarism scan request. |
| `similarWords` | array<object> | Similar words identified in the input text. |
| `sources` | array<object> | Matched sources found during the scan. |
| `status` | number | HTTP status code returned by Winston AI. |
| `text` | string | Input text used for the plagiarism scan. |

## Native endpoint

Through the native Winston AI API, this operation is `POST /v2/plagiarism` (base URL `https://api.gowinston.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-plagiarism.md) for the provider-specific parameters and requirements.

