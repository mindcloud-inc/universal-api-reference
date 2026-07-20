# OpenPLZ Universal API Examples

These examples use the MindCloud API key and OpenPLZ connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Full Text Search Austria



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/full-text-search-austria?connectionId=$CONNECTION_ID&limit=25&offset=0&searchTerm=Wien%20Stephansplatz" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "searchTerm": "Wien Stephansplatz"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/full-text-search-austria?${params}`, {
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
      "district": {},
      "federalProvince": {},
      "key": "string",
      "locality": "string",
      "municipality": {},
      "name": "Ava Chen",
      "postalCode": "string"
    }
  ],
  "meta": {}
}
```

See the full [Full Text Search Austria action reference](actions/full-text-search-austria.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openPLZ/latest/actions/full-text-search-austria).
