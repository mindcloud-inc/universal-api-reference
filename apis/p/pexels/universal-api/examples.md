# Pexels Universal API Examples

These examples use the MindCloud API key and Pexels connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Photos

Finds photos in Pexels by search query.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pexels/latest/actions/search-photos?connectionId=$CONNECTION_ID&limit=25&offset=0&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pexels/latest/actions/search-photos?${params}`, {
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
      "next_page": "string",
      "page": 1,
      "per_page": 1,
      "photos": [
        {}
      ],
      "prev_page": "string",
      "total_results": 1
    }
  ],
  "meta": {}
}
```

See the full [Search Photos action reference](actions/search-photos.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pexels/latest/actions/search-photos).
