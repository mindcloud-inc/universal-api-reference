# MealDB Universal API Examples

These examples use the MindCloud API key and MealDB connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Filter Meals by Area



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mealDB/latest/actions/filter-meals-by-area?connectionId=$CONNECTION_ID&area=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "area": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mealDB/latest/actions/filter-meals-by-area?${params}`, {
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
      "meals": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Filter Meals by Area action reference](actions/filter-meals-by-area.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mealDB/latest/actions/filter-meals-by-area).
