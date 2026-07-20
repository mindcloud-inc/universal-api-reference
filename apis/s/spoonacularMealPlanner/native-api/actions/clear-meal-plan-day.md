# Clear Meal Plan Day with Spoonacular Meal Planner

Deletes all meal plan items for a day from Spoonacular Meal Planner.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/mealplanner/{username}/day/{date}`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Clear Meal Plan Day](https://spoonacular.com/food-api/docs#Clear-Meal-Plan-Day)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `string` | no | Date in yyyy-mm-dd format. |
| `hash` | query | `string` | no | Private hash returned by Connect User. |
| `username` | path | `string` | no | Spoonacular username returned by Connect User. |
