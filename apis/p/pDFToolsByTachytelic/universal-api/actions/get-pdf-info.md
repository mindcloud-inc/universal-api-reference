# PDF Tools by Tachytelic: Get PDF Info



```
GET https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/get-pdf-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF Tools by Tachytelic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/get-pdf-info?connectionId=$CONNECTION_ID&pdfFileContent=Base64%20PDF%20content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pdfFileContent": "Base64 PDF content"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/get-pdf-info?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "Author": "string",
      "CreationDate": "string",
      "Creator": "string",
      "HasText": true,
      "IsEncrypted": true,
      "Keywords": "string",
      "ModDate": "string",
      "PageCount": 1,
      "PDFVersion": "string",
      "Producer": "string",
      "Subject": "string",
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Author` | string | PDF author metadata. |
| `CreationDate` | string | PDF creation date metadata. |
| `Creator` | string | PDF creator metadata. |
| `HasText` | boolean | Whether extractable text is present. |
| `IsEncrypted` | boolean | Whether the PDF is encrypted. |
| `Keywords` | string | PDF keyword metadata. |
| `ModDate` | string | PDF modification date metadata. |
| `PageCount` | number | Number of pages in the PDF. |
| `PDFVersion` | string | PDF version reported by the API. |
| `Producer` | string | PDF producer metadata. |
| `Subject` | string | PDF subject metadata. |
| `Title` | string | PDF title metadata. |

## Native endpoint

Through the native PDF Tools by Tachytelic API, this operation is `POST /getinfo` (base URL `https://pdf.tachytelic.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pdf-info.md) for the provider-specific parameters and requirements.

