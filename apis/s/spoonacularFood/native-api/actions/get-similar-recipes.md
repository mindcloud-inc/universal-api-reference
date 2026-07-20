# Get Similar Recipes with Spoonacular Food

Retrieves similar recipes from Spoonacular Food.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/:id/similar`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Similar Recipes](https://spoonacular.com/food-api/docs#Get-Similar-Recipes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The source recipe ID used to find similar recipes. |
