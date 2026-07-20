# Add Meal Plan Template with Spoonacular

Creates a meal plan template in Spoonacular.

## Endpoint

- **Method:** `POST`
- **Path:** `/mealplanner/{username}/templates`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Add Meal Plan Template](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | yes | Required by the Spoonacular endpoint. |
| `username` | path | `string` | yes | Required by the Spoonacular endpoint. |
