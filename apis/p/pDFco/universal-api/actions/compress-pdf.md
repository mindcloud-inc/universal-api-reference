# PDF.co: Compress PDF

Compresses a PDF in PDF.co.

```
PUT https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/compress-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/compress-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://pdfco-test-files.s3.us-west-2.amazonaws.com/pdf-compress/sample.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/compress-pdf', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://pdfco-test-files.s3.us-west-2.amazonaws.com/pdf-compress/sample.pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Source PDF URL accessible by PDF.co. Example: `https://pdfco-test-files.s3.us-west-2.amazonaws.com/pdf-compress/sample.pdf`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `async` | boolean | no | Set true to run as async job. Example: `false`. |
| `name` | string | no | Optional output filename. Example: `compressed.pdf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits": 1,
      "duration": 1,
      "error": true,
      "name": "Ava Chen",
      "outputLinkValidTill": "https://example.com",
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
| `credits` | number |  |
| `duration` | number |  |
| `error` | boolean |  |
| `name` | string |  |
| `outputLinkValidTill` | string |  |
| `pageCount` | number |  |
| `remainingCredits` | number |  |
| `status` | number |  |
| `url` | string |  |

## Native endpoint

Through the native PDF.co API, this operation is `POST /../v2/pdf/compress` (base URL `https://api.pdf.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compress-pdf.md) for the provider-specific parameters and requirements.

