# DeepAI Universal API Examples

These examples use the MindCloud API key and DeepAI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Colorize Image

Creates a colorized image in DeepAI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepAI/latest/actions/colorize-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image": "https://example.com/image.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepAI/latest/actions/colorize-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "image": "https://example.com/image.jpg"
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

See the full [Colorize Image action reference](actions/colorize-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deepAI/latest/actions/colorize-image).
