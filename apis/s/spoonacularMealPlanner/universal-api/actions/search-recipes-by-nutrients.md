# Spoonacular Meal Planner: Search Recipes by Nutrients

Finds recipes in Spoonacular Meal Planner by nutrient ranges.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/search-recipes-by-nutrients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Meal Planner `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/search-recipes-by-nutrients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/search-recipes-by-nutrients?${params}`, {
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
| `maxCalories` | number | no | Maximum calories per serving. |
| `maxFat` | string | no | Maximum fat grams per serving. |
| `maxProtein` | number | no | Maximum protein grams per serving. |
| `minCalories` | number | no | Minimum calories per serving. |
| `minProtein` | number | no | Minimum protein grams per serving. |
| `random` | boolean | no | Return a random set within requested nutrient limits. |

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
      "imageType": "string",
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
| `imageType` | string |  |
| `protein` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Spoonacular Meal Planner API, this operation is `GET /recipes/findByNutrients` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-recipes-by-nutrients.md) for the provider-specific parameters and requirements.

