# PDF-app: Compress PDF

Creates a compressed PDF in PDF-app.

```
POST https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/compress-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/compress-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/compress-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileUrl` | string | yes | Public URL of the PDF to compress. |
| `pdfSettings` | string | no | Compression profile such as /screen, /ebook, /printer, or /prepress. |
| `async` | boolean | no | Set true to run compression asynchronously. |
| `fileName` | string | no | Optional output file name for the compressed PDF. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jpegQuality` | number | no | Optional JPEG quality setting for image recompression. |

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
      "presignedUrl": [
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
| `creditsConsumed` | number | Credits consumed by the operation. |
| `creditsRemaining` | number | Remaining PDF-app credits after the operation. |
| `jobId` | string | Job identifier returned by PDF-app. |
| `message` | string | Provider success message. |
| `presignedUrl` | array<string> | Temporary download URL array for the compressed PDF. |

## Native endpoint

Through the native PDF-app API, this operation is `POST /compress_PDF` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compress-pdf.md) for the provider-specific parameters and requirements.

