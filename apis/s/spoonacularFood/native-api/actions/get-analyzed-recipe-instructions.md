# Get Analyzed Recipe Instructions with Spoonacular Food

Retrieves analyzed recipe instructions from Spoonacular Food.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/:id/analyzedInstructions`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Analyzed Recipe Instructions](https://spoonacular.com/food-api/docs#Get-Analyzed-Recipe-Instructions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Spoonacular recipe ID. |
| `stepBreakdown` | query | `boolean` | no | Whether to break down the recipe steps further. |
