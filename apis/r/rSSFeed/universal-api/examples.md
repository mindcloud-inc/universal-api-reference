# RSS Feed Universal API Examples

These examples use the MindCloud API key and RSS Feed connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Feed Items

Retrieves items from the configured RSS feed.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rSSFeed/latest/actions/list-feed-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rSSFeed/latest/actions/list-feed-items?${params}`, {
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
      "author": "string",
      "description": "string",
      "guid": "string",
      "link": "https://example.com",
      "pubDate": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Feed Items action reference](actions/list-feed-items.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rSSFeed/latest/actions/list-feed-items).
