# Autocomplete Recipes with Spoonacular Food

Finds recipe suggestions in Spoonacular Food by partial title.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/autocomplete`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Autocomplete Recipes](https://spoonacular.com/food-api/docs#Autocomplete-Recipe-Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Recipe name prefix to autocomplete. |
