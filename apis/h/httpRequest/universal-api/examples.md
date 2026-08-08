# HTTP Universal API Examples

These examples use the MindCloud API key and HTTP connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Send HTTP Request

Sends an HTTP request to any URL.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/httpRequest/latest/actions/send-http-request?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com%2Fpath%3Fquery%3Dvalue&method=DELETE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com/path?query=value",
  "method": "DELETE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/httpRequest/latest/actions/send-http-request?${params}`, {
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

See the full [Send HTTP Request action reference](actions/send-http-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/httpRequest/latest/actions/send-http-request).
