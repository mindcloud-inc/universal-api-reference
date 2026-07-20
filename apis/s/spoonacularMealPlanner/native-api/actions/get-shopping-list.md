# Get Shopping List with Spoonacular Meal Planner

Retrieves a shopping list from Spoonacular Meal Planner.

## Endpoint

- **Method:** `GET`
- **Path:** `/mealplanner/{username}/shopping-list`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Shopping List](https://spoonacular.com/food-api/docs#Get-Shopping-List)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | no | Private hash returned by Connect User. |
| `username` | path | `string` | no | Spoonacular username returned by Connect User. |
