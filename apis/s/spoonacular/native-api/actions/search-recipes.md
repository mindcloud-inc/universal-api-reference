# Search Recipes with Spoonacular

Searches Spoonacular recipes with advanced filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/complexSearch`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Search Recipes](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addRecipeNutrition` | query | `string` | no | Include recipe nutrition in the results. |
| `cuisine` | query | `string` | no | One or more cuisines, comma separated. |
| `diet` | query | `string` | no | Restrict recipes to a diet. |
| `number` | query | `string` | no | The number of recipes to return. |
| `offset` | query | `string` | no | How many matching recipes to skip. |
| `query` | query | `string` | no | The natural language recipe search query. |
