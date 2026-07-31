# SWAPI Universal API Examples

These examples use the MindCloud API key and SWAPI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Film



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sWAPI/latest/actions/get-film?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sWAPI/latest/actions/get-film?${params}`, {
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
      "characters": [
        "string"
      ],
      "director": "string",
      "episode_id": 1,
      "opening_crawl": "string",
      "producer": "string",
      "release_date": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Film action reference](actions/get-film.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sWAPI/latest/actions/get-film).
