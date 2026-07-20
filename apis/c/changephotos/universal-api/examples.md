# change.photos Universal API Examples

These examples use the MindCloud API key and change.photos connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Adjust Image Quality

Creates an image with adjusted quality in change.photos.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/changephotos/latest/actions/adjust-image-quality" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/photo.jpg",
  "quality": "80"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/changephotos/latest/actions/adjust-image-quality', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/photo.jpg",
    "quality": "80"
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
      "compression": {},
      "format": "string",
      "height": 1,
      "original": {},
      "processed": {},
      "transformations": {},
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

See the full [Adjust Image Quality action reference](actions/adjust-image-quality.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/changephotos/latest/actions/adjust-image-quality).
