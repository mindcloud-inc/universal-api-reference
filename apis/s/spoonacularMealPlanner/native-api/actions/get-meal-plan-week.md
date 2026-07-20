# Get Meal Plan Week with Spoonacular Meal Planner

Retrieves a weekly meal plan from Spoonacular Meal Planner.

## Endpoint

- **Method:** `GET`
- **Path:** `/mealplanner/{username}/week/{start-date}`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Meal Plan Week](https://spoonacular.com/food-api/docs#Get-Meal-Plan-Week)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | no | Private hash returned by Connect User. |
| `start-date` | path | `string` | no | Week start date in yyyy-mm-dd format. |
| `username` | path | `string` | no | Spoonacular username returned by Connect User. |
