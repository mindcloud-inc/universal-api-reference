# PDF-app: Convert PDF To DOCX

Creates a DOCX file from a PDF in PDF-app.

```
POST https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/convert-pdf-to-docx
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/convert-pdf-to-docx" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pdfUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/convert-pdf-to-docx', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pdfUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pdfUrl` | string | yes | Public URL of the PDF file to convert to DOCX. |
| `async` | boolean | no | Set true to queue the conversion asynchronously. |
| `fileName` | string | no | Optional output file name for the DOCX file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsConsumed": 1,
      "creditsRemaining": 1,
      "jobId": "string",
      "message": "string",
      "presignedUrls": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsConsumed` | number |  |
| `creditsRemaining` | number |  |
| `jobId` | string |  |
| `message` | string |  |
| `presignedUrls` | array<string> |  |

## Native endpoint

Through the native PDF-app API, this operation is `POST /pdf_to_docx2` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-pdf-to-docx.md) for the provider-specific parameters and requirements.

