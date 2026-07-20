# Delete from Shopping List with Spoonacular

Deletes an item from a Spoonacular shopping list.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/mealplanner/{username}/shopping-list/items/{id}`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Delete from Shopping List](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | yes | Required by the Spoonacular endpoint. |
| `id` | path | `string` | yes | Required by the Spoonacular endpoint. |
| `username` | path | `string` | yes | Required by the Spoonacular endpoint. |
