# Apple Map Links Universal API Examples

These examples use the MindCloud API key and Apple Map Links connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Frame Map

Frames a map view in Apple Maps.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/frame-map?connectionId=$CONNECTION_ID&center=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "center": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/frame-map?${params}`, {
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
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Frame Map action reference](actions/frame-map.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/appleMapLinks/latest/actions/frame-map).
