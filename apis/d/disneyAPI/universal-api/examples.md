# Disney API Universal API Examples

These examples use the MindCloud API key and Disney API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Character



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/disneyAPI/latest/actions/get-character?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/disneyAPI/latest/actions/get-character?${params}`, {
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
      "data": {
        "_id": 1,
        "films": [
          "string"
        ],
        "imageUrl": "https://example.com",
        "name": "Ava Chen",
        "shortFilms": [
          "string"
        ],
        "sourceUrl": "https://example.com",
        "tvShows": [
          "string"
        ],
        "url": "https://example.com",
        "videoGames": [
          "string"
        ]
      },
      "info": {
        "count": 1,
        "nextPage": "string",
        "previousPage": "string",
        "totalPages": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Character action reference](actions/get-character.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/disneyAPI/latest/actions/get-character).
