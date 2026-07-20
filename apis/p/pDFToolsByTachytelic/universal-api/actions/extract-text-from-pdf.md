# PDF Tools by Tachytelic: Extract Text from PDF



```
GET https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/extract-text-from-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF Tools by Tachytelic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/extract-text-from-pdf?connectionId=$CONNECTION_ID&pdfFileContent=Base64%20PDF%20content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pdfFileContent": "Base64 PDF content"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/extract-text-from-pdf?${params}`, {
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
| `pdfFileContent` | string | yes | Base64-encoded PDF file content. Example: `Base64 PDF content`. |
| `startPage` | number | no | Optional page number to start text extraction from. Example: `1`. |
| `endPage` | number | no | Optional page number to stop text extraction at, inclusive. Example: `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ExtractedText": "string",
      "ExtractedTextByPage": [
        {
          "Page": 1,
          "Text": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ExtractedText` | string | Combined text extracted from the selected PDF pages. |
| `ExtractedTextByPage` | array<object> | Text extracted from each page. |
| `ExtractedTextByPage[].Page` | number | Page number for this extracted text entry. |
| `ExtractedTextByPage[].Text` | string | Text extracted from this page. |

## Native endpoint

Through the native PDF Tools by Tachytelic API, this operation is `POST /extracttext` (base URL `https://pdf.tachytelic.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-text-from-pdf.md) for the provider-specific parameters and requirements.

