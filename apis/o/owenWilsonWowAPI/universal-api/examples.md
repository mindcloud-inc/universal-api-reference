# Owen Wilson Wow API Universal API Examples

These examples use the MindCloud API key and Owen Wilson Wow API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Ordered Wow



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/owenWilsonWowAPI/latest/actions/get-ordered-wow?connectionId=$CONNECTION_ID&index=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "index": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/owenWilsonWowAPI/latest/actions/get-ordered-wow?${params}`, {
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
      "audio": "https://example.com",
      "character": "string",
      "current_wow_in_movie": 1,
      "director": "string",
      "full_line": "string",
      "movie": "string",
      "movie_duration": "string",
      "poster": "https://example.com",
      "release_date": "string",
      "timestamp": "string",
      "total_wows_in_movie": 1,
      "video": {},
      "year": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Ordered Wow action reference](actions/get-ordered-wow.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/owenWilsonWowAPI/latest/actions/get-ordered-wow).
