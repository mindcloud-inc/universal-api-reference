# Add to Shopping List with Spoonacular

Adds an item to a Spoonacular shopping list.

## Endpoint

- **Method:** `POST`
- **Path:** `/mealplanner/{username}/shopping-list/items`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Add to Shopping List](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | yes | Required by the Spoonacular endpoint. |
| `username` | path | `string` | yes | Required by the Spoonacular endpoint. |
