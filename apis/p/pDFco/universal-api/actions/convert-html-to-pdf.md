# PDF.co: Convert HTML to PDF

Creates a PDF from HTML in PDF.co.

```
POST https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/convert-html-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/convert-html-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "html": "<html><body>Hello PDF.co</body></html>"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/convert-html-to-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "html": "<html><body>Hello PDF.co</body></html>"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `html` | string | yes | Source HTML content to convert into PDF. Example: `<html><body>Hello PDF.co</body></html>`. |
| `name` | string | no | Optional output file name. Example: `result.pdf`. |

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

Through the native PDF.co API, this operation is `POST /pdf/convert/from/html` (base URL `https://api.pdf.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-html-to-pdf.md) for the provider-specific parameters and requirements.

