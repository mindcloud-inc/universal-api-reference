# Perigon Universal API Examples

These examples use the MindCloud API key and Perigon connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Articles

Finds news articles in Perigon by keywords and filters.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-articles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-articles?${params}`, {
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
      "articles": [
        {}
      ],
      "numResults": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Search Articles action reference](actions/search-articles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/perigon/latest/actions/search-articles).
