# Delete from Meal Plan with Spoonacular Meal Planner

Deletes a meal plan item from Spoonacular Meal Planner.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/mealplanner/{username}/items/{id}`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Delete from Meal Plan](https://spoonacular.com/food-api/docs#Delete-from-Meal-Plan)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | no | Private hash returned by Connect User. |
| `id` | path | `string` | no | Meal plan item ID. |
| `username` | path | `string` | no | Spoonacular username returned by Connect User. |
