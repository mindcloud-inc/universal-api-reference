# Spoonacular Meal Planner: Search Recipes by Ingredients

Finds recipes in Spoonacular Meal Planner by ingredients.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/search-recipes-by-ingredients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Meal Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/search-recipes-by-ingredients?connectionId=$CONNECTION_ID&ingredients=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ingredients": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/search-recipes-by-ingredients?${params}`, {
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
| `ignorePantry` | boolean | no | Ignore typical pantry items. |
| `ingredients` | string | yes | Comma-separated ingredients that recipes should contain. |
| `ranking` | number | no | Rank by maximizing used ingredients (1) or minimizing missing ingredients (2). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "image": "string",
      "imageType": "string",
      "likes": 1,
      "missedIngredientCount": 1,
      "missedIngredients": [
        {}
      ],
      "title": "string",
      "unusedIngredients": [
        {}
      ],
      "usedIngredientCount": 1,
      "usedIngredients": [
        {}
      ]
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
| `likes` | number |  |
| `missedIngredientCount` | number |  |
| `missedIngredients` | array<object> |  |
| `title` | string |  |
| `unusedIngredients` | array<object> |  |
| `usedIngredientCount` | number |  |
| `usedIngredients` | array<object> |  |

## Native endpoint

Through the native Spoonacular Meal Planner API, this operation is `GET /recipes/findByIngredients` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-recipes-by-ingredients.md) for the provider-specific parameters and requirements.

