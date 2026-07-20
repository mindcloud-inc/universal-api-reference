# GNews Universal API Examples

These examples use the MindCloud API key and GNews connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Top Headlines

Retrieves current top news headlines from GNews.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gNews/latest/actions/list-top-headlines?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gNews/latest/actions/list-top-headlines?${params}`, {
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
      "content": "string",
      "description": "string",
      "id": "string",
      "image": "string",
      "lang": "string",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "source": {
        "id": "string",
        "name": "Ava Chen",
        "url": "https://example.com"
      },
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Top Headlines action reference](actions/list-top-headlines.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gNews/latest/actions/list-top-headlines).
