# Get Ingredient Substitutes with Spoonacular

Retrieves ingredient substitutes from Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/ingredients/substitutes`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Ingredient Substitutes](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ingredientName` | query | `string` | yes | Required by the Spoonacular endpoint. |
