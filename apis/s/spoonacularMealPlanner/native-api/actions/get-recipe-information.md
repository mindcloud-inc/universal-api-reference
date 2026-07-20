# Get Recipe Information with Spoonacular Meal Planner

Retrieves recipe details from Spoonacular Meal Planner.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/{id}/information`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Recipe Information](https://spoonacular.com/food-api/docs#Get-Recipe-Information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Recipe ID. |
| `includeNutrition` | query | `boolean` | no | Include nutrition data in the response. |
