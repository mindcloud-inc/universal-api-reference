# Yeti Snow Universal API Examples

These examples use the MindCloud API key and Yeti Snow connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sites



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/list-sites?${params}`, {
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
      "count": 1,
      "sites": {}
    }
  ],
  "meta": {}
}
```

See the full [List Sites action reference](actions/list-sites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/yetiSnow/latest/actions/list-sites).
