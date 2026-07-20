# Nutrition by ID with Spoonacular

Retrieves nutrition data for a Spoonacular recipe.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/{id}/nutritionWidget.json`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Nutrition by ID](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Required by the Spoonacular endpoint. |
