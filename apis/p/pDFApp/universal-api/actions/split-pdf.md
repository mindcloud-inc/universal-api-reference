# PDF-app: Split PDF

Creates split PDF files in PDF-app.

```
POST https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/split-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/split-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileUrl": "https://example.com",
  "pagesPerSplit": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/split-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileUrl": "https://example.com",
    "pagesPerSplit": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileUrl` | string | yes | Public URL of the PDF to split. |
| `pagesPerSplit` | number | yes | Number of pages to include in each split PDF. |
| `async` | boolean | no | Set true to run the split asynchronously. |
| `fileName` | string | no | Optional base file name for the split outputs. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageRanges` | string | no | Optional custom page ranges to split, such as 1-2,4-5. |

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
| `creditsConsumed` | number | Credits consumed by the operation. |
| `creditsRemaining` | number | Remaining PDF-app credits after the operation. |
| `jobId` | string | Job identifier returned by PDF-app. |
| `message` | string | Provider success message. |
| `presignedUrls` | array<string> | Temporary download URLs for the split PDF files. |

## Native endpoint

Through the native PDF-app API, this operation is `POST /splitt_PDF` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/split-pdf.md) for the provider-specific parameters and requirements.

