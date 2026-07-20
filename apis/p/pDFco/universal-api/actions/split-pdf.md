# PDF.co: Split PDF

Creates split PDF files in PDF.co.

```
POST https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/split-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/split-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/split-pdf', {
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
| `url` | string | yes | URL of PDF file to split. |
| `name` | string | no | Optional output filename. |
| `async` | boolean | no | Process split as background job. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pages` | string | no | Pages or page ranges to extract. |

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
      "outputLinkValidTill": "2026-05-07T12:00:00.000Z",
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
| `credits` | number | Credits consumed. |
| `duration` | number | Processing duration in ms. |
| `error` | boolean | Whether split failed. |
| `name` | string | Requested output filename. |
| `outputLinkValidTill` | date | Expiration timestamp for output URLs. |
| `pageCount` | number | Total pages in split output. |
| `remainingCredits` | number | Credits left in account. |
| `status` | number | Status code from PDF.co. |
| `urls` | array<string> | Output URLs for each split part. |

## Native endpoint

Through the native PDF.co API, this operation is `POST /pdf/split` (base URL `https://api.pdf.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/split-pdf.md) for the provider-specific parameters and requirements.

