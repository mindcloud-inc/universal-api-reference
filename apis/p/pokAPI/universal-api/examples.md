# PokéAPI Universal API Examples

These examples use the MindCloud API key and PokéAPI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Pokemon

Retrieves pokemon from PokéAPI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/list-pokemon?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/list-pokemon?${params}`, {
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
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Pokemon action reference](actions/list-pokemon.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pokAPI/latest/actions/list-pokemon).
