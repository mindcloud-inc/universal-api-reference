# Summarize Recipe with Spoonacular Food

Retrieves a recipe summary from Spoonacular Food.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/:id/summary`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Summarize Recipe](https://spoonacular.com/food-api/docs#Summarize-Recipe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Spoonacular recipe ID. |
