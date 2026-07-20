# PDFBolt: Create PDF Link from HTML

Creates a PDF download link from HTML in PDFBolt.

```
POST https://connect.mindcloud.co/v1/universal/pDFBolt/latest/actions/create-pdf-link-from-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDFBolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFBolt/latest/actions/create-pdf-link-from-html" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "html": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFBolt/latest/actions/create-pdf-link-from-html', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "html": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `html` | string | yes | Base64-encoded HTML content to convert into a PDF link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentSizeMb": 1,
      "documentUrl": "https://example.com",
      "duration": 1,
      "errorCode": "string",
      "errorMessage": "string",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "isAsync": true,
      "isCustomS3Bucket": true,
      "requestId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentSizeMb` | number | Generated PDF size in megabytes. |
| `documentUrl` | string | Temporary download URL for the generated PDF. |
| `duration` | number | Conversion duration in milliseconds. |
| `errorCode` | string | Provider error code when the conversion fails. |
| `errorMessage` | string | Provider error message when the conversion fails. |
| `expiresAt` | date | When the temporary download URL expires. |
| `isAsync` | boolean | Whether the conversion completed asynchronously. |
| `isCustomS3Bucket` | boolean | Whether the file was stored in a custom S3 bucket. |
| `requestId` | string | The PDFBolt request identifier for the conversion. |
| `status` | string | The conversion status returned by PDFBolt. |

## Native endpoint

Through the native PDFBolt API, this operation is `POST /sync` (base URL `https://api.pdfbolt.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pdf-link-from-html.md) for the provider-specific parameters and requirements.

