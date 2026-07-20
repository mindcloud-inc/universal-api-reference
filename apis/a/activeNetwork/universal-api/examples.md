# Active Network Universal API Examples

These examples use the MindCloud API key and Active Network connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Assets

Finds activity assets in Active Network.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/search-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/search-assets?${params}`, {
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

See the full [Search Assets action reference](actions/search-assets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/activeNetwork/latest/actions/search-assets).
