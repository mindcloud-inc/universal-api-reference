# PDFCrowd Universal API Examples

These examples use the MindCloud API key and PDFCrowd connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Combine PDF Files

Creates one PDF from multiple PDF files in PDFCrowd.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFCrowd/latest/actions/combine-pdf-files" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "f_1": "string",
  "f_2": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFCrowd/latest/actions/combine-pdf-files', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "f_1": "string",
    "f_2": "string"
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

See the full [Combine PDF Files action reference](actions/combine-pdf-files.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pDFCrowd/latest/actions/combine-pdf-files).
