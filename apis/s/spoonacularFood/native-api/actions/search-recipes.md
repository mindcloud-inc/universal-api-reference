# Search Recipes with Spoonacular Food

Finds recipes in Spoonacular Food by keyword.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/complexSearch`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Search Recipes](https://spoonacular.com/food-api/docs#Search-Recipes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Natural language recipe search query. |
