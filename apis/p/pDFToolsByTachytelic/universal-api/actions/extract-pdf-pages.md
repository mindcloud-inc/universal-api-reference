# PDF Tools by Tachytelic: Extract PDF Pages



```
GET https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/extract-pdf-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF Tools by Tachytelic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/extract-pdf-pages?connectionId=$CONNECTION_ID&pdfFileContent=Base64%20PDF%20content&pageRange=1-3%2C7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pdfFileContent": "Base64 PDF content",
  "pageRange": "1-3,7"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/extract-pdf-pages?${params}`, {
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
| `pageRange` | string | yes | Page range to extract, for example 1-3,7. Example: `1-3,7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ExtractedPdf": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ExtractedPdf` | string | Base64-encoded PDF containing the requested pages. |

## Native endpoint

Through the native PDF Tools by Tachytelic API, this operation is `POST /extractpages` (base URL `https://pdf.tachytelic.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-pdf-pages.md) for the provider-specific parameters and requirements.

