# Spoonacular Recipe: Search Recipes by Ingredients

Finds recipes in Spoonacular by ingredients.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/search-recipes-by-ingredients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Recipe `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/search-recipes-by-ingredients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/search-recipes-by-ingredients?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "image": "string",
      "imageType": "string",
      "missedIngredientCount": 1,
      "title": "string",
      "usedIngredientCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `image` | string |  |
| `imageType` | string |  |
| `missedIngredientCount` | number |  |
| `title` | string |  |
| `usedIngredientCount` | number |  |

## Native endpoint

Through the native Spoonacular Recipe API, this operation is `GET /recipes/findByIngredients` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-recipes-by-ingredients.md) for the provider-specific parameters and requirements.

