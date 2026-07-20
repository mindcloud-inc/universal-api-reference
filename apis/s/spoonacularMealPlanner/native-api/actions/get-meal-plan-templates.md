# Get Meal Plan Templates with Spoonacular Meal Planner

Retrieves meal plan templates from Spoonacular Meal Planner.

## Endpoint

- **Method:** `GET`
- **Path:** `/mealplanner/{username}/templates`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Meal Plan Templates](https://spoonacular.com/food-api/docs#Get-Meal-Plan-Templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | no | Private hash returned by Connect User. |
| `username` | path | `string` | no | Spoonacular username returned by Connect User. |
