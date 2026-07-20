# Add to Meal Plan with Spoonacular

Adds an item to a Spoonacular meal plan.

## Endpoint

- **Method:** `POST`
- **Path:** `/mealplanner/{username}/items`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Add to Meal Plan](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | yes | Required by the Spoonacular endpoint. |
| `username` | path | `string` | yes | Required by the Spoonacular endpoint. |
