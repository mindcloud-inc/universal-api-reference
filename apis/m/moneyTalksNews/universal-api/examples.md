# Money Talks News Universal API Examples

These examples use the MindCloud API key and Money Talks News connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Site Feed Items



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moneyTalksNews/latest/actions/list-site-feed-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moneyTalksNews/latest/actions/list-site-feed-items?${params}`, {
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
      "pubDate": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Site Feed Items action reference](actions/list-site-feed-items.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moneyTalksNews/latest/actions/list-site-feed-items).
