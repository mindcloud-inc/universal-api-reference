# Search Recipes by Ingredients with Spoonacular Meal Planner

Finds recipes in Spoonacular Meal Planner by ingredients.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/findByIngredients`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Search Recipes by Ingredients](https://spoonacular.com/food-api/docs#Search-Recipes-by-Ingredients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ignorePantry` | query | `boolean` | no | Ignore typical pantry items. |
| `ingredients` | query | `string` | yes | Comma-separated ingredients that recipes should contain. |
| `ranking` | query | `number` | no | Rank by maximizing used ingredients (1) or minimizing missing ingredients (2). |
