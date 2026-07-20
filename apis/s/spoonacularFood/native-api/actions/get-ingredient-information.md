# Get Ingredient Information with Spoonacular Food

Retrieves ingredient information from Spoonacular Food.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/ingredients/:id/information`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Ingredient Information](https://spoonacular.com/food-api/docs#Get-Ingredient-Information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Spoonacular ingredient ID. |
| `amount` | query | `number` | no | Amount of the ingredient. |
