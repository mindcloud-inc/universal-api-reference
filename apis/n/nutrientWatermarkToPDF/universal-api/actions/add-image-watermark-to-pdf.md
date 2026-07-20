# Nutrient - Watermark to PDF: Add Image Watermark to PDF

Updates a PDF with an image watermark in Nutrient.

```
PUT https://connect.mindcloud.co/v1/universal/nutrientWatermarkToPDF/latest/actions/add-image-watermark-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient - Watermark to PDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nutrientWatermarkToPDF/latest/actions/add-image-watermark-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document": "string",
  "logo": "string",
  "instructions": {
    "parts": [
      {
        "file": "document"
      }
    ],
    "actions": [
      {
        "type": "watermark",
        "image": "logo",
        "width": "50%"
      }
    ]
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nutrientWatermarkToPDF/latest/actions/add-image-watermark-to-pdf', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document": "string",
    "logo": "string",
    "instructions": {"parts":[{"file":"document"}],"actions":[{"type":"watermark","image":"logo","width":"50%"}]}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `document` | file | yes | PDF file to watermark. |
| `logo` | file | yes | Image file to use as the watermark. |
| `instructions` | object | yes | Build instructions for an image watermark. The image key must match the Logo Image field. Default: `{"parts":[{"file":"document"}],"actions":[{"type":"watermark","image":"logo","width":"50%"}]}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resultPdf": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resultPdf` | string | Processed PDF returned by Nutrient. |

## Native endpoint

Through the native Nutrient - Watermark to PDF API, this operation is `POST /build` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-image-watermark-to-pdf.md) for the provider-specific parameters and requirements.

