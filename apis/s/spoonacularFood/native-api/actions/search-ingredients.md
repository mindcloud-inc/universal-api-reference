# Search Ingredients with Spoonacular Food

Finds ingredients in Spoonacular Food by keyword.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/ingredients/search`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Search Ingredients](https://spoonacular.com/food-api/docs#Ingredient-Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Ingredient search query. |
