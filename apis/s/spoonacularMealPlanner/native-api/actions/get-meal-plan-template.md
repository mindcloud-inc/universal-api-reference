# Get Meal Plan Template with Spoonacular Meal Planner

Retrieves a meal plan template from Spoonacular Meal Planner.

## Endpoint

- **Method:** `GET`
- **Path:** `/mealplanner/{username}/templates/{id}`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Meal Plan Template](https://spoonacular.com/food-api/docs#Get-Meal-Plan-Template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | no | Private hash returned by Connect User. |
| `id` | path | `string` | no | Meal plan template ID. |
| `username` | path | `string` | no | Spoonacular username returned by Connect User. |
