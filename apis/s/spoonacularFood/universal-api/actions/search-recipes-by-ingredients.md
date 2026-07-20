# Spoonacular Food: Search Recipes by Ingredients

Finds recipes in Spoonacular Food by ingredient list.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/search-recipes-by-ingredients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Food `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/search-recipes-by-ingredients?connectionId=$CONNECTION_ID&ingredients=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ingredients": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/search-recipes-by-ingredients?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ingredients` | string | yes | Comma-separated ingredient names that recipes should contain. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "image": "string",
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
| `missedIngredientCount` | number |  |
| `title` | string |  |
| `usedIngredientCount` | number |  |

## Native endpoint

Through the native Spoonacular Food API, this operation is `GET /recipes/findByIngredients` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-recipes-by-ingredients.md) for the provider-specific parameters and requirements.

