# Nutrient - Watermark to PDF Universal API Examples

These examples use the MindCloud API key and Nutrient - Watermark to PDF connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Add Image Watermark to PDF

Updates a PDF with an image watermark in Nutrient.

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

Example response:

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

See the full [Add Image Watermark to PDF action reference](actions/add-image-watermark-to-pdf.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nutrientWatermarkToPDF/latest/actions/add-image-watermark-to-pdf).
