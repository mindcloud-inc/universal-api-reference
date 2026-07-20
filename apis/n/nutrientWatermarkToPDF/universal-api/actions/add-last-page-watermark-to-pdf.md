# Nutrient - Watermark to PDF: Add Last Page Watermark to PDF

Updates the last PDF page with a watermark in Nutrient.

```
PUT https://connect.mindcloud.co/v1/universal/nutrientWatermarkToPDF/latest/actions/add-last-page-watermark-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient - Watermark to PDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nutrientWatermarkToPDF/latest/actions/add-last-page-watermark-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document": "string",
  "logo": "string",
  "instructions": {
    "parts": [
      {
        "file": "document",
        "pages": {
          "end": -2
        }
      },
      {
        "file": "document",
        "pages": {
          "start": -1
        },
        "actions": [
          {
            "type": "watermark",
            "image": "logo",
            "width": "50%"
          }
        ]
      }
    ]
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nutrientWatermarkToPDF/latest/actions/add-last-page-watermark-to-pdf', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document": "string",
    "logo": "string",
    "instructions": {"parts":[{"file":"document","pages":{"end":-2}},{"file":"document","pages":{"start":-1},"actions":[{"type":"watermark","image":"logo","width":"50%"}]}]}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `document` | file | yes | PDF file to watermark. |
| `logo` | file | yes | Image file to apply on the last page. |
| `instructions` | object | yes | Build instructions that leave earlier pages unchanged and apply an image watermark to only the last page. Default: `{"parts":[{"file":"document","pages":{"end":-2}},{"file":"document","pages":{"start":-1},"actions":[{"type":"watermark","image":"logo","width":"50%"}]}]}`. |

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

Through the native Nutrient - Watermark to PDF API, this operation is `POST /build` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-last-page-watermark-to-pdf.md) for the provider-specific parameters and requirements.

