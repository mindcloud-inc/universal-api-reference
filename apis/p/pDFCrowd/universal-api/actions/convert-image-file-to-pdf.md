# PDFCrowd: Convert Image File to PDF

Creates a PDF from an image file in PDFCrowd.

```
POST https://connect.mindcloud.co/v1/universal/pDFCrowd/latest/actions/convert-image-file-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDFCrowd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFCrowd/latest/actions/convert-image-file-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFCrowd/latest/actions/convert-image-file-to-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Image file to upload and convert into a PDF. |

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

Through the native PDFCrowd API, this operation is `POST https://api.pdfcrowd.com/convert/24.04/` (base URL `https://api.pdfcrowd.com/convert/24.04/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-image-file-to-pdf.md) for the provider-specific parameters and requirements.

