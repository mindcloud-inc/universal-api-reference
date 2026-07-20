# Get Shopping List with Spoonacular

Retrieves a shopping list from Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/mealplanner/{username}/shopping-list`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Shopping List](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | no | Required by the Spoonacular endpoint. |
| `username` | path | `string` | yes | Required by the Spoonacular endpoint. |
