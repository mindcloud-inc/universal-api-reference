# APImage Universal API Examples

These examples use the MindCloud API key and APImage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Analyze Image

Extracts text from an image with APImage.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aPImage/latest/actions/analyze-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image_url": "https://example.com/image.png",
  "prompt": "List the objects and text visible in the image."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aPImage/latest/actions/analyze-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "image_url": "https://example.com/image.png",
    "prompt": "List the objects and text visible in the image."
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

See the full [Analyze Image action reference](actions/analyze-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aPImage/latest/actions/analyze-image).
