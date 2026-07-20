# Get Meal Plan Week with Spoonacular

Retrieves a weekly meal plan from Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/mealplanner/{username}/week/{start-date}`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Meal Plan Week](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | yes | Required by the Spoonacular endpoint. |
| `start-date` | path | `string` | yes | Required by the Spoonacular endpoint. |
| `username` | path | `string` | yes | Required by the Spoonacular endpoint. |
