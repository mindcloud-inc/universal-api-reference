# Delete Meal Plan Template with Spoonacular

Deletes a meal plan template from Spoonacular.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/mealplanner/{username}/templates/{id}`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Delete Meal Plan Template](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | yes | Required by the Spoonacular endpoint. |
| `id` | path | `string` | yes | Required by the Spoonacular endpoint. |
| `username` | path | `string` | yes | Required by the Spoonacular endpoint. |
