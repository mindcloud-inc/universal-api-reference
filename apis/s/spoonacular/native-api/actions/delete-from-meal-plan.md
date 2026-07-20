# Delete from Meal Plan with Spoonacular

Deletes an item from a Spoonacular meal plan.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/mealplanner/{username}/items/{id}`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Delete from Meal Plan](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | yes | Required by the Spoonacular endpoint. |
| `id` | path | `string` | yes | Required by the Spoonacular endpoint. |
| `username` | path | `string` | yes | Required by the Spoonacular endpoint. |
