# Compute Ingredient Amount with Spoonacular

Computes an amount for a Spoonacular ingredient.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/ingredients/{id}/amount`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Compute Ingredient Amount](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Required by the Spoonacular endpoint. |
| `nutrient` | query | `string` | yes | Required by the Spoonacular endpoint. |
| `target` | query | `string` | yes | Required by the Spoonacular endpoint. |
