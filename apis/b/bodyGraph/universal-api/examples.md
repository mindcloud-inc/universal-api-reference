# BodyGraph Universal API Examples

These examples use the MindCloud API key and BodyGraph connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Locations

Finds locations in BodyGraph by search term.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bodyGraph/latest/actions/search-locations?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bodyGraph/latest/actions/search-locations?${params}`, {
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
      "admin1": "string",
      "asciiname": "Ava Chen",
      "country": "string",
      "geo": "string",
      "timezone": "string",
      "tokens": [
        "string"
      ],
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Search Locations action reference](actions/search-locations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bodyGraph/latest/actions/search-locations).
