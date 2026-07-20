# PDF.co: PDF to Text

Creates text from a PDF in PDF.co.

```
POST https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/pdf-to-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/pdf-to-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/pdf-to-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | URL of PDF file to convert. |
| `async` | boolean | no | Process conversion as background job. |
| `name` | string | no | Optional output filename. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pages` | string | no | Optional page range (e.g. 1-3). |
| `password` | string | no | Password for protected PDFs. |
| `lang` | string | no | Language hint for OCR parsing. |
| `inline` | boolean | no | Return text inline when true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits": 1,
      "duration": 1,
      "error": true,
      "jobId": "string",
      "name": "Ava Chen",
      "outputLinkValidTill": "2026-05-07T12:00:00.000Z",
      "pageCount": 1,
      "remainingCredits": 1,
      "status": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | number | Credits consumed. |
| `duration` | number | Processing duration in ms. |
| `error` | boolean | Whether conversion failed. |
| `jobId` | string | Background job ID when async=true. |
| `name` | string | Output filename. |
| `outputLinkValidTill` | date | Expiration time for output URL. |
| `pageCount` | number | Pages processed. |
| `remainingCredits` | number | Credits left in account. |
| `status` | number | Status code returned by PDF.co. |
| `url` | string | Temporary URL for converted text output. |

## Native endpoint

Through the native PDF.co API, this operation is `POST /pdf/convert/to/text` (base URL `https://api.pdf.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pdf-to-text.md) for the provider-specific parameters and requirements.

