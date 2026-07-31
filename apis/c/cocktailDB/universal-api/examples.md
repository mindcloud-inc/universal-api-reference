# CocktailDB Universal API Examples

These examples use the MindCloud API key and CocktailDB connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Filter Cocktails by Alcoholic Status



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cocktailDB/latest/actions/filter-cocktails-by-alcoholic-status?connectionId=$CONNECTION_ID&alcoholicStatus=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "alcoholicStatus": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cocktailDB/latest/actions/filter-cocktails-by-alcoholic-status?${params}`, {
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
      "drinks": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Filter Cocktails by Alcoholic Status action reference](actions/filter-cocktails-by-alcoholic-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cocktailDB/latest/actions/filter-cocktails-by-alcoholic-status).
