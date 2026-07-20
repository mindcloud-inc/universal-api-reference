# Nutrient - Watermark to PDF: Add Page Range Watermark to PDF

Updates selected PDF pages with a watermark in Nutrient.

```
PUT https://connect.mindcloud.co/v1/universal/nutrientWatermarkToPDF/latest/actions/add-page-range-watermark-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient - Watermark to PDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nutrientWatermarkToPDF/latest/actions/add-page-range-watermark-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document": "string",
  "instructions": {
    "parts": [
      {
        "file": "document",
        "pages": {
          "end": 0,
          "start": 0
        },
        "actions": [
          {
            "left": 0,
            "text": "Confidential",
            "type": "watermark",
            "width": 250,
            "bottom": "100%",
            "height": 100,
            "opacity": 0.4,
            "fontSize": 36,
            "fontColor": "#FF0000",
            "fontFamily": "Helvetica"
          }
        ]
      }
    ]
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nutrientWatermarkToPDF/latest/actions/add-page-range-watermark-to-pdf', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document": "string",
    "instructions": {"parts":[{"file":"document","pages":{"end":0,"start":0},"actions":[{"left":0,"text":"Confidential","type":"watermark","width":250,"bottom":"100%","height":100,"opacity":0.4,"fontSize":36,"fontColor":"#FF0000","fontFamily":"Helvetica"}]}]}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `document` | file | yes | PDF file to watermark. |
| `instructions` | object | yes | Build instructions with a page selection. Adjust pages.start and pages.end to choose the target range. Default: `{"parts":[{"file":"document","pages":{"end":0,"start":0},"actions":[{"left":0,"text":"Confidential","type":"watermark","width":250,"bottom":"100%","height":100,"opacity":0.4,"fontSize":36,"fontColor":"#FF0000","fontFamily":"Helvetica"}]}]}`. |

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

Through the native Nutrient - Watermark to PDF API, this operation is `POST /build` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-page-range-watermark-to-pdf.md) for the provider-specific parameters and requirements.

