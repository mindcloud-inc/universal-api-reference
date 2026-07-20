# DynamicPDF Universal API Examples

These examples use the MindCloud API key and DynamicPDF connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Convert PDF To Image

Converts a PDF to images in DynamicPDF API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/convert-pdf-to-image?connectionId=$CONNECTION_ID&pdf=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pdf": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/convert-pdf-to-image?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "horizontalDpi": 1,
      "images": [
        {
          "billedPages": 1,
          "data": "string",
          "height": 1,
          "pageNumber": "string",
          "width": 1
        }
      ],
      "verticalDpi": 1
    }
  ],
  "meta": {}
}
```

See the full [Convert PDF To Image action reference](actions/convert-pdf-to-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dynamicPDFAPI/latest/actions/convert-pdf-to-image).

## Add Barcode To Existing PDF

Adds a barcode to an existing PDF in DynamicPDF API.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/add-barcode-to-existing-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "instructions": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/add-barcode-to-existing-pdf', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "instructions": {}
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
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Barcode To Existing PDF action reference](actions/add-barcode-to-existing-pdf.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dynamicPDFAPI/latest/actions/add-barcode-to-existing-pdf).
