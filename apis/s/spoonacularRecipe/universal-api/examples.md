# Spoonacular Recipe Universal API Examples

These examples use the MindCloud API key and Spoonacular Recipe connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Recipes

Finds recipes in Spoonacular with advanced filters.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/search-recipes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/search-recipes?${params}`, {
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
      "id": 1,
      "image": "string",
      "imageType": "string",
      "readyInMinutes": 1,
      "servings": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Search Recipes action reference](actions/search-recipes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/spoonacularRecipe/latest/actions/search-recipes).
