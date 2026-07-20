# Get Recipe Information with Spoonacular Food

Retrieves recipe information from Spoonacular Food.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/:id/information`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Recipe Information](https://spoonacular.com/food-api/docs#Get-Recipe-Information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Spoonacular recipe ID. |
| `includeNutrition` | query | `boolean` | no | Whether to include nutrition data in the recipe information. |
