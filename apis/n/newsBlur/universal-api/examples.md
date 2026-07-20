# NewsBlur Universal API Examples

These examples use the MindCloud API key and NewsBlur connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Autocomplete Feeds

Finds feeds in NewsBlur by search phrase.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/autocomplete-feeds?connectionId=$CONNECTION_ID&term=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "term": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/autocomplete-feeds?${params}`, {
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
      "feeds": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Autocomplete Feeds action reference](actions/autocomplete-feeds.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/newsBlur/latest/actions/autocomplete-feeds).

## Add Feed

Adds a feed to NewsBlur.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/add-feed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/add-feed', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
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
      "authenticated": true,
      "code": 1,
      "feed": {},
      "folder": "string",
      "message": "string",
      "result": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Feed action reference](actions/add-feed.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/newsBlur/latest/actions/add-feed).
