# Generate Shopping List with Spoonacular Meal Planner

Creates a shopping list from a meal plan in Spoonacular Meal Planner.

## Endpoint

- **Method:** `POST`
- **Path:** `/mealplanner/{username}/shopping-list/{start-date}/{end-date}`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Generate Shopping List](https://spoonacular.com/food-api/docs#Generate-Shopping-List)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end-date` | path | `string` | no | Shopping-list end date in yyyy-mm-dd format. |
| `hash` | query | `string` | no | Private hash returned by Connect User. |
| `start-date` | path | `string` | no | Shopping-list start date in yyyy-mm-dd format. |
| `username` | path | `string` | no | Spoonacular username returned by Connect User. |
