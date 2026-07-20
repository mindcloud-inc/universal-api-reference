# Generate Meal Plan with Spoonacular Meal Planner

Retrieves a generated meal plan from Spoonacular Meal Planner.

## Endpoint

- **Method:** `GET`
- **Path:** `/mealplanner/generate`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Generate Meal Plan](https://spoonacular.com/food-api/docs#Generate-Meal-Plan)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `diet` | query | `string` | no | Diet preference such as vegetarian, vegan, or ketogenic. |
| `exclude` | query | `string` | no | Comma-separated ingredients to exclude. |
| `targetCalories` | query | `number` | no | Daily calorie target for the generated plan. |
| `timeFrame` | query | `string` | no | Meal plan time frame: day or week. |
