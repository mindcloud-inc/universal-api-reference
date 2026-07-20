# Autocomplete Ingredient Search with Spoonacular

Autocompletes ingredient names in Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/ingredients/autocomplete`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Autocomplete Ingredient Search](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Required by the Spoonacular endpoint. |
