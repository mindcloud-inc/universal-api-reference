# Delete from Shopping List with Spoonacular Meal Planner

Deletes a shopping list item from Spoonacular Meal Planner.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/mealplanner/{username}/shopping-list/items/{id}`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Delete from Shopping List](https://spoonacular.com/food-api/docs#Delete-from-Shopping-List)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | no | Private hash returned by Connect User. |
| `id` | path | `string` | no | Shopping list item ID. |
| `username` | path | `string` | no | Spoonacular username returned by Connect User. |
