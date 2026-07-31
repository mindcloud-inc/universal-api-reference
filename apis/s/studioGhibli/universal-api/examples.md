# Studio Ghibli Universal API Examples

These examples use the MindCloud API key and Studio Ghibli connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Film by ID



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/get-film-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/get-film-by-id?${params}`, {
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
      "director": "string",
      "id": "string",
      "image": "string",
      "locations": [
        "string"
      ],
      "movie_banner": "string",
      "original_title": "string",
      "original_title_romanised": "string",
      "people": [
        "string"
      ],
      "producer": "string",
      "release_date": "string",
      "rt_score": "string",
      "running_time": "string",
      "species": [
        "string"
      ],
      "title": "string",
      "url": "https://example.com",
      "vehicles": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Film by ID action reference](actions/get-film-by-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/studioGhibli/latest/actions/get-film-by-id).
