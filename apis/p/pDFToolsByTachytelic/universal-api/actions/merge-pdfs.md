# PDF Tools by Tachytelic: Merge PDFs



```
GET https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/merge-pdfs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF Tools by Tachytelic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/merge-pdfs?connectionId=$CONNECTION_ID&pdfFiles%5B%5D=base64Pdf1%2Cbase64Pdf2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pdfFiles[]": "base64Pdf1,base64Pdf2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/merge-pdfs?${params}`, {
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
| `pdfFiles[]` | array<string> | yes | Array of base64-encoded PDF files to merge. Accepts multiple values as an array. Example: `base64Pdf1,base64Pdf2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "MergedPdf": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `MergedPdf` | string | Base64-encoded merged PDF. |

## Native endpoint

Through the native PDF Tools by Tachytelic API, this operation is `POST /merge` (base URL `https://pdf.tachytelic.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-pdfs.md) for the provider-specific parameters and requirements.

