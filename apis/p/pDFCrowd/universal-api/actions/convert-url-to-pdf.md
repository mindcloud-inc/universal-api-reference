# PDFCrowd: Convert URL to PDF

Creates a PDF from a URL in PDFCrowd.

```
POST https://connect.mindcloud.co/v1/universal/pDFCrowd/latest/actions/convert-url-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDFCrowd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFCrowd/latest/actions/convert-url-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFCrowd/latest/actions/convert-url-to-pdf', {
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
| `url` | string | yes | Public web page URL to convert into a PDF. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `failOnMainUrlError` | boolean | no | Abort the conversion when the main URL returns an HTTP error status. Default: `true`. |
| `contentViewportWidth` | string | no | Viewport width used when rendering the page before conversion. Default: `balanced`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        [
          1
        ]
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<number> |  |
| `type` | string |  |

## Native endpoint

Through the native PDFCrowd API, this operation is `POST https://api.pdfcrowd.com/convert/24.04/` (base URL `https://api.pdfcrowd.com/convert/24.04/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-url-to-pdf.md) for the provider-specific parameters and requirements.

