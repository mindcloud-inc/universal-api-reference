# Memix Universal API Examples

These examples use the MindCloud API key and Memix connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate GIF Memix

Retrieves a generated GIF from Memix.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memix/latest/actions/generate-gif-memix?connectionId=$CONNECTION_ID&template_slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template_slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memix/latest/actions/generate-gif-memix?${params}`, {
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

See the full [Generate GIF Memix action reference](actions/generate-gif-memix.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/memix/latest/actions/generate-gif-memix).
