# PDF Blocks Universal API Examples

These examples use the MindCloud API key and PDF Blocks connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Add Image Watermark

Updates a PDF document with an image watermark in PDF Blocks.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pDFBlocks/latest/actions/add-image-watermark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "image": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFBlocks/latest/actions/add-image-watermark', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "image": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Image Watermark action reference](actions/add-image-watermark.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pDFBlocks/latest/actions/add-image-watermark).
