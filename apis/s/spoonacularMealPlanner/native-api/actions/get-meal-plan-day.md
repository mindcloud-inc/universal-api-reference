# Get Meal Plan Day with Spoonacular Meal Planner

Retrieves a daily meal plan from Spoonacular Meal Planner.

## Endpoint

- **Method:** `GET`
- **Path:** `/mealplanner/{username}/day/{date}`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Meal Plan Day](https://spoonacular.com/food-api/docs#Get-Meal-Plan-Day)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `string` | no | Date in yyyy-mm-dd format. |
| `hash` | query | `string` | no | Private hash returned by Connect User. |
| `username` | path | `string` | no | Spoonacular username returned by Connect User. |
