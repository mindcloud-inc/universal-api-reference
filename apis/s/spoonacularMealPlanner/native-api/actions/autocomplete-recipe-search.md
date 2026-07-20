# Autocomplete Recipe Search with Spoonacular Meal Planner

Finds recipe suggestions in Spoonacular Meal Planner by title prefix.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/autocomplete`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Autocomplete Recipe Search](https://spoonacular.com/food-api/docs#Autocomplete-Recipe-Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Recipe title prefix or search term. |
