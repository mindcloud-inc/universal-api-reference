# Clear Meal Plan Day with Spoonacular

Clears a day from a Spoonacular meal plan.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/mealplanner/{username}/day/{date}`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Clear Meal Plan Day](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `string` | yes | Required by the Spoonacular endpoint. |
| `hash` | query | `string` | yes | Required by the Spoonacular endpoint. |
| `username` | path | `string` | yes | Required by the Spoonacular endpoint. |
