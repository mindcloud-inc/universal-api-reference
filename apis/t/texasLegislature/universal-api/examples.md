# Texas Legislature Universal API Examples

These examples use the MindCloud API key and Texas Legislature connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Today's Bill Analyses RSS Feed

Retrieves today's bill analyses from Texas Legislature.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/texasLegislature/latest/actions/get-todays-bill-analyses-rss-feed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/texasLegislature/latest/actions/get-todays-bill-analyses-rss-feed?${params}`, {
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

See the full [Get Today's Bill Analyses RSS Feed action reference](actions/get-todays-bill-analyses-rss-feed.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/texasLegislature/latest/actions/get-todays-bill-analyses-rss-feed).
