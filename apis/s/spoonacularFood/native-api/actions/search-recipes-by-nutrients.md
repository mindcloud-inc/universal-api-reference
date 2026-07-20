# Search Recipes by Nutrients with Spoonacular Food

Finds recipes in Spoonacular Food by nutrient limits.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/findByNutrients`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Search Recipes by Nutrients](https://spoonacular.com/food-api/docs#Search-Recipes-by-Nutrients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `maxCalories` | query | `number` | no | Maximum calories per serving. |
