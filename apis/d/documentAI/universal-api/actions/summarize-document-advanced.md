# Document AI: Summarize Document Advanced



```
GET https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/summarize-document-advanced
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/summarize-document-advanced?connectionId=$CONNECTION_ID&InputFile=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "InputFile": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/summarize-document-advanced?${params}`, {
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
| `InputFile` | string | yes | Base64-encoded document content to summarize. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `RecognitionMode` | string | no | OCR recognition mode. Default: `Advanced`. |
| `Language` | string | no | Language code for summarization. Default: `ENG`. |
| `SummaryParagraphCount` | number | no | Number of paragraphs to include in the summary. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confidenceScore": 1,
      "documentSummaryText": "string",
      "successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confidenceScore` | number | Summary confidence score. |
| `documentSummaryText` | string | Generated document summary. |
| `successful` | boolean | Whether advanced summarization succeeded. |

## Native endpoint

Through the native Document AI API, this operation is `POST /document-ai/document/extract/summary/advanced` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/summarize-document-advanced.md) for the provider-specific parameters and requirements.

