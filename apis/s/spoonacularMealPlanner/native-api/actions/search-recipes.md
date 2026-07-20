# Search Recipes with Spoonacular Meal Planner

Finds recipes in Spoonacular Meal Planner by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/complexSearch`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Search Recipes](https://spoonacular.com/food-api/docs#Search-Recipes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addRecipeInformation` | query | `string` | no | Include full recipe information in search results. |
| `addRecipeNutrition` | query | `string` | no | Include nutritional information in search results. |
| `cuisine` | query | `string` | no | Cuisine filter; multiple values may be comma-separated. |
| `diet` | query | `string` | no | Diet filter such as vegetarian, vegan, or gluten free. |
| `excludeIngredients` | query | `string` | no | Comma-separated ingredients recipes must not contain. |
| `includeIngredients` | query | `string` | no | Comma-separated ingredients that recipes should include. |
| `intolerances` | query | `string` | no | Comma-separated intolerances that recipes must avoid. |
| `maxReadyTime` | query | `number` | no | Maximum preparation and cook time in minutes. |
| `query` | query | `string` | no | Natural-language recipe search query. |
| `sort` | query | `string` | no | Spoonacular recipe sort option. |
| `sortDirection` | query | `string` | no | Sort direction: asc or desc. |
| `type` | query | `string` | no | Recipe type such as main course, dessert, or breakfast. |
