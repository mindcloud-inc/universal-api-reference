# Search Recipes by Ingredients with Spoonacular Food

Finds recipes in Spoonacular Food by ingredient list.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/findByIngredients`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Search Recipes by Ingredients](https://spoonacular.com/food-api/docs#Search-Recipes-by-Ingredients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ingredients` | query | `string` | yes | Comma-separated ingredient names that recipes should contain. |
