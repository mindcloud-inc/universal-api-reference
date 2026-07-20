# Get Meal Plan Templates with Spoonacular

Retrieves meal plan templates from Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/mealplanner/{username}/templates`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Meal Plan Templates](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | yes | Required by the Spoonacular endpoint. |
| `username` | path | `string` | yes | Required by the Spoonacular endpoint. |
