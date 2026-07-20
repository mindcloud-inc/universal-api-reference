# Spoonacular Meal Planner: Get Recipe Information

Retrieves recipe details from Spoonacular Meal Planner.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/get-recipe-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Meal Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/get-recipe-information?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/get-recipe-information?${params}`, {
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
| `id` | number | yes | Recipe ID. |
| `includeNutrition` | boolean | no | Include nutrition data in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extendedIngredients": [
        {}
      ],
      "glutenFree": true,
      "id": 1,
      "image": "string",
      "imageType": "string",
      "readyInMinutes": 1,
      "servings": 1,
      "sourceUrl": "https://example.com",
      "summary": "string",
      "title": "string",
      "vegan": true,
      "vegetarian": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extendedIngredients` | array<object> |  |
| `glutenFree` | boolean |  |
| `id` | number |  |
| `image` | string |  |
| `imageType` | string |  |
| `readyInMinutes` | number |  |
| `servings` | number |  |
| `sourceUrl` | string |  |
| `summary` | string |  |
| `title` | string |  |
| `vegan` | boolean |  |
| `vegetarian` | boolean |  |

## Native endpoint

Through the native Spoonacular Meal Planner API, this operation is `GET /recipes/{id}/information` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recipe-information.md) for the provider-specific parameters and requirements.

