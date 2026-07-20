# Convert Ingredient Amount with Spoonacular Food

Converts ingredient amounts in Spoonacular Food.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/convert`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Convert Ingredient Amount](https://spoonacular.com/food-api/docs#Convert-Amounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ingredientName` | query | `string` | yes | Ingredient to convert. |
| `sourceAmount` | query | `number` | yes | Amount to convert from. |
| `sourceUnit` | query | `string` | yes | Unit to convert from. |
| `targetUnit` | query | `string` | yes | Unit to convert to. |
