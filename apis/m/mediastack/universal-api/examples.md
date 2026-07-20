# Mediastack Universal API Examples

These examples use the MindCloud API key and Mediastack connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search News

Finds news articles in Mediastack.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mediastack/latest/actions/search-news?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mediastack/latest/actions/search-news?${params}`, {
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
      "category": "string",
      "country": "string",
      "description": "string",
      "image": "https://example.com",
      "language": "string",
      "published_at": "2026-05-07T12:00:00.000Z",
      "source": "Ava Chen",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Search News action reference](actions/search-news.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mediastack/latest/actions/search-news).
