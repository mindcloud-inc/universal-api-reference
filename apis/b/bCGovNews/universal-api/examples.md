# BC Gov News Universal API Examples

These examples use the MindCloud API key and BC Gov News connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Agriculture and Food News

Retrieves Agriculture and Food announcements from BC Gov News.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bCGovNews/latest/actions/list-agriculture-and-food-news?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bCGovNews/latest/actions/list-agriculture-and-food-news?${params}`, {
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
      "category": "string",
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

See the full [List Agriculture and Food News action reference](actions/list-agriculture-and-food-news.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bCGovNews/latest/actions/list-agriculture-and-food-news).
