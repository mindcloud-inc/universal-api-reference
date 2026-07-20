# Formatting Universal API Examples

These examples use the MindCloud API key and Formatting connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Encode URL

Encodes a URL string in the Formatting app.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formatting/latest/actions/encode-url?connectionId=$CONNECTION_ID&input=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formatting/latest/actions/encode-url?${params}`, {
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
      "encodedUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Encode URL action reference](actions/encode-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/formatting/latest/actions/encode-url).
