# Shibe.online Universal API Examples

These examples use the MindCloud API key and Shibe.online connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Random Bird Images



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shibeonline/latest/actions/get-random-bird-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shibeonline/latest/actions/get-random-bird-images?${params}`, {
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

See the full [Get Random Bird Images action reference](actions/get-random-bird-images.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shibeonline/latest/actions/get-random-bird-images).
