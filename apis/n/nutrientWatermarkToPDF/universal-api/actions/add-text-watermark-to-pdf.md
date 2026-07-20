# Nutrient - Watermark to PDF: Add Text Watermark to PDF

Updates a PDF with a text watermark in Nutrient.

```
PUT https://connect.mindcloud.co/v1/universal/nutrientWatermarkToPDF/latest/actions/add-text-watermark-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient - Watermark to PDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nutrientWatermarkToPDF/latest/actions/add-text-watermark-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document": "string",
  "instructions": {
    "parts": [
      {
        "file": "document"
      }
    ],
    "actions": [
      {
        "left": 0,
        "text": "Property of Nutrient",
        "type": "watermark",
        "width": 250,
        "bottom": "100%",
        "height": 200,
        "opacity": 0.5,
        "fontSize": 50,
        "rotation": 10,
        "fontColor": "#FF0000",
        "fontStyle": [
          "italic",
          "bold"
        ],
        "fontFamily": "Helvetica"
      }
    ]
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nutrientWatermarkToPDF/latest/actions/add-text-watermark-to-pdf', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document": "string",
    "instructions": {"parts":[{"file":"document"}],"actions":[{"left":0,"text":"Property of Nutrient","type":"watermark","width":250,"bottom":"100%","height":200,"opacity":0.5,"fontSize":50,"rotation":10,"fontColor":"#FF0000","fontStyle":["italic","bold"],"fontFamily":"Helvetica"}]}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `document` | file | yes | PDF file to watermark. |
| `instructions` | object | yes | Build instructions for a text watermark. Edit the text, position, color, opacity, or dimensions as needed. Default: `{"parts":[{"file":"document"}],"actions":[{"left":0,"text":"Property of Nutrient","type":"watermark","width":250,"bottom":"100%","height":200,"opacity":0.5,"fontSize":50,"rotation":10,"fontColor":"#FF0000","fontStyle":["italic","bold"],"fontFamily":"Helvetica"}]}`. |

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

Through the native Nutrient - Watermark to PDF API, this operation is `POST /build` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-text-watermark-to-pdf.md) for the provider-specific parameters and requirements.

