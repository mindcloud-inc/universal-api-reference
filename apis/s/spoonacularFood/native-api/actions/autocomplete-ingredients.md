# Autocomplete Ingredients with Spoonacular Food

Finds ingredient suggestions in Spoonacular Food by partial name.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/ingredients/autocomplete`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Autocomplete Ingredients](https://spoonacular.com/food-api/docs#Autocomplete-Ingredient-Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Partial or full ingredient name. |
