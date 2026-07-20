# Search Recipes by Nutrients with Spoonacular Meal Planner

Finds recipes in Spoonacular Meal Planner by nutrient ranges.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/findByNutrients`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Search Recipes by Nutrients](https://spoonacular.com/food-api/docs#Search-Recipes-by-Nutrients)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `maxCalories` | query | `number` | no | Maximum calories per serving. |
| `maxFat` | query | `string` | no | Maximum fat grams per serving. |
| `maxProtein` | query | `number` | no | Maximum protein grams per serving. |
| `minCalories` | query | `number` | no | Minimum calories per serving. |
| `minProtein` | query | `number` | no | Minimum protein grams per serving. |
| `random` | query | `boolean` | no | Return a random set within requested nutrient limits. |
