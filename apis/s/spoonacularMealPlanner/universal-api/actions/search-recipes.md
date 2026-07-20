# Spoonacular Meal Planner: Search Recipes

Finds recipes in Spoonacular Meal Planner by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/search-recipes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Meal Planner `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/search-recipes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/search-recipes?${params}`, {
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
| `addRecipeInformation` | string | no | Include full recipe information in search results. |
| `addRecipeNutrition` | string | no | Include nutritional information in search results. |
| `cuisine` | string | no | Cuisine filter; multiple values may be comma-separated. |
| `diet` | string | no | Diet filter such as vegetarian, vegan, or gluten free. |
| `excludeIngredients` | string | no | Comma-separated ingredients recipes must not contain. |
| `includeIngredients` | string | no | Comma-separated ingredients that recipes should include. |
| `intolerances` | string | no | Comma-separated intolerances that recipes must avoid. |
| `maxReadyTime` | number | no | Maximum preparation and cook time in minutes. |
| `query` | string | no | Natural-language recipe search query. |
| `sort` | string | no | Spoonacular recipe sort option. |
| `sortDirection` | string | no | Sort direction: asc or desc. |
| `type` | string | no | Recipe type such as main course, dessert, or breakfast. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "number": 1,
      "offset": 1,
      "results": [
        {}
      ],
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `number` | number |  |
| `offset` | number |  |
| `results` | array<object> | Matching recipes. |
| `totalResults` | number |  |

## Native endpoint

Through the native Spoonacular Meal Planner API, this operation is `GET /recipes/complexSearch` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-recipes.md) for the provider-specific parameters and requirements.

