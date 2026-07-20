# Icon Horse Universal API Examples

These examples use the MindCloud API key and Icon Horse connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Icon

Retrieves a website icon from Icon Horse by hostname.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iconHorse/latest/actions/get-icon?connectionId=$CONNECTION_ID&hostname=github.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hostname": "github.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iconHorse/latest/actions/get-icon?${params}`, {
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

See the full [Get Icon action reference](actions/get-icon.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iconHorse/latest/actions/get-icon).
