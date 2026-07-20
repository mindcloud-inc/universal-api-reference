# Generate Shopping List with Spoonacular

Generates a shopping list in Spoonacular.

## Endpoint

- **Method:** `POST`
- **Path:** `/mealplanner/{username}/shopping-list/{start-date}/{end-date}`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Generate Shopping List](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end-date` | path | `string` | yes | Required by the Spoonacular endpoint. |
| `hash` | query | `string` | yes | Required by the Spoonacular endpoint. |
| `start-date` | path | `string` | yes | Required by the Spoonacular endpoint. |
| `username` | path | `string` | yes | Required by the Spoonacular endpoint. |
