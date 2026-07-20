# Delete Meal Plan Template with Spoonacular Meal Planner

Deletes a meal plan template from Spoonacular Meal Planner.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/mealplanner/{username}/templates/{id}`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Delete Meal Plan Template](https://spoonacular.com/food-api/docs#Delete-Meal-Plan-Template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | no | Private hash returned by Connect User. |
| `id` | path | `string` | no | Meal plan template ID. |
| `username` | path | `string` | no | Spoonacular username returned by Connect User. |
