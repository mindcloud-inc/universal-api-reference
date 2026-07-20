# World News API Universal API Examples

These examples use the MindCloud API key and World News API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search News

Finds news articles in World News API by filter criteria.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/search-news?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/search-news?${params}`, {
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
      "available": 1,
      "news": [
        {}
      ],
      "number": 1,
      "offset": 1
    }
  ],
  "meta": {}
}
```

See the full [Search News action reference](actions/search-news.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/worldNewsAPI/latest/actions/search-news).

## Suggest News Source

Creates a news source suggestion in World News API.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/suggest-news-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://www.cnn.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/suggest-news-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://www.cnn.com"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Suggest News Source action reference](actions/suggest-news-source.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/worldNewsAPI/latest/actions/suggest-news-source).
