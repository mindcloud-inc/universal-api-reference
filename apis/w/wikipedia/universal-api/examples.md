# Wikipedia Universal API Examples

These examples use the MindCloud API key and Wikipedia connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Pages

Finds pages in Wikipedia by search query.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wikipedia/latest/actions/search-pages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wikipedia/latest/actions/search-pages?${params}`, {
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
      "batchcomplete": true,
      "continue": {},
      "query": {}
    }
  ],
  "meta": {}
}
```

See the full [Search Pages action reference](actions/search-pages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wikipedia/latest/actions/search-pages).
