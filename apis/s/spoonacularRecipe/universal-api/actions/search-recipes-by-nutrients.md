# Spoonacular Recipe: Search Recipes by Nutrients

Finds recipes in Spoonacular by nutrient constraints.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/search-recipes-by-nutrients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Recipe `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/search-recipes-by-nutrients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/search-recipes-by-nutrients?${params}`, {
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
      "calories": 1,
      "carbs": "string",
      "fat": "string",
      "id": 1,
      "image": "string",
      "protein": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calories` | number |  |
| `carbs` | string |  |
| `fat` | string |  |
| `id` | number |  |
| `image` | string |  |
| `protein` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Spoonacular Recipe API, this operation is `GET /recipes/findByNutrients` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-recipes-by-nutrients.md) for the provider-specific parameters and requirements.

