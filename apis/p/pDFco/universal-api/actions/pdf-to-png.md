# PDF.co: PDF to PNG

Converts a PDF to PNG in PDF.co.

```
GET https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/pdf-to-png
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/pdf-to-png?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fpdfco-test-files.s3.us-west-2.amazonaws.com%2Fpdf-compress%2Fsample.pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://pdfco-test-files.s3.us-west-2.amazonaws.com/pdf-compress/sample.pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/pdf-to-png?${params}`, {
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
| `url` | string | yes | Source PDF URL. Example: `https://pdfco-test-files.s3.us-west-2.amazonaws.com/pdf-compress/sample.pdf`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pages` | string | no | Optional page selection. Example: `1`. |
| `async` | boolean | no | Set true to run as async job. Example: `false`. |

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
      "urls": [
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
| `credits` | number |  |
| `duration` | number |  |
| `error` | boolean |  |
| `name` | string |  |
| `outputLinkValidTill` | string |  |
| `pageCount` | number |  |
| `remainingCredits` | number |  |
| `status` | number |  |
| `urls` | array<string> |  |

## Native endpoint

Through the native PDF.co API, this operation is `POST /pdf/convert/to/png` (base URL `https://api.pdf.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pdf-to-png.md) for the provider-specific parameters and requirements.

