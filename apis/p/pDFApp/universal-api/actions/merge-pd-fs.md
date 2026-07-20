# PDF-app: Merge PDFs

Creates a merged PDF in PDF-app.

```
POST https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/merge-pd-fs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/merge-pd-fs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pdfUrls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/merge-pd-fs', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pdfUrls[]": ["https://example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pdfUrls[]` | array<string> | yes | Public URLs of the PDF files to merge in order. |
| `async` | boolean | no | Set true to queue the merge asynchronously. |
| `fileName` | string | no | Optional output file name for the merged PDF. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsConsumed": 1,
      "creditsRemaining": 1,
      "jobId": "string",
      "mergedPdfUrl": "https://example.com",
      "message": "string"
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
| `mergedPdfUrl` | string | Temporary download URL for the merged PDF. |
| `message` | string | Provider success message. |

## Native endpoint

Through the native PDF-app API, this operation is `POST /merge_pdf` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-pd-fs.md) for the provider-specific parameters and requirements.

