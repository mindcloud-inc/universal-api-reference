# Spoonacular Meal Planner: Generate Meal Plan

Retrieves a generated meal plan from Spoonacular Meal Planner.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/generate-meal-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Meal Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/generate-meal-plan?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/generate-meal-plan?${params}`, {
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
| `diet` | string | no | Diet preference such as vegetarian, vegan, or ketogenic. |
| `exclude` | string | no | Comma-separated ingredients to exclude. |
| `targetCalories` | number | no | Daily calorie target for the generated plan. |
| `timeFrame` | string | no | Meal plan time frame: day or week. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meals": [
        {}
      ],
      "nutrients": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meals` | array<object> | Generated meal entries. |
| `nutrients` | object | Daily nutrient summary. |

## Native endpoint

Through the native Spoonacular Meal Planner API, this operation is `GET /mealplanner/generate` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-meal-plan.md) for the provider-specific parameters and requirements.

