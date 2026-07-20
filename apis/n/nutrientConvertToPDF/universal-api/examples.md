# Nutrient - Convert to PDF Universal API Examples

These examples use the MindCloud API key and Nutrient - Convert to PDF connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Convert HTML File to PDF

Creates a PDF document from an HTML file in Nutrient.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nutrientConvertToPDF/latest/actions/convert-html-file-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nutrientConvertToPDF/latest/actions/convert-html-file-to-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "pdf": "string"
    }
  ],
  "meta": {}
}
```

See the full [Convert HTML File to PDF action reference](actions/convert-html-file-to-pdf.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nutrientConvertToPDF/latest/actions/convert-html-file-to-pdf).
