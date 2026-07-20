# Get Ingredient Substitutes with Spoonacular Food

Retrieves ingredient substitutes from Spoonacular Food.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/ingredients/substitutes`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Ingredient Substitutes](https://spoonacular.com/food-api/docs#Get-Ingredient-Substitutes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ingredientName` | query | `string` | yes | Ingredient to find substitutes for. |
