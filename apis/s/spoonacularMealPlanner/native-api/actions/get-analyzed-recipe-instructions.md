# Get Analyzed Recipe Instructions with Spoonacular Meal Planner

Retrieves analyzed recipe instructions from Spoonacular Meal Planner.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/{id}/analyzedInstructions`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Analyzed Recipe Instructions](https://spoonacular.com/food-api/docs#Get-Analyzed-Recipe-Instructions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Recipe ID. |
| `stepBreakdown` | query | `boolean` | no | Break analyzed instructions into steps. |
