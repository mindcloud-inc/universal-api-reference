# SCRNIFY.com Universal API Examples

These examples use the MindCloud API key and SCRNIFY.com connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Capture Screenshot or Video

Captures a screenshot or video with SCRNIFY.com.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sCRNIFYcom/latest/actions/capture-screenshot-or-video?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com&format=0&type=0&width=1280" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com",
  "format": "0",
  "type": "0",
  "width": "1280"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sCRNIFYcom/latest/actions/capture-screenshot-or-video?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Capture Screenshot or Video action reference](actions/capture-screenshot-or-video.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sCRNIFYcom/latest/actions/capture-screenshot-or-video).
