# Get Recipe Nutrition with Spoonacular Food

Retrieves recipe nutrition data from Spoonacular Food.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/:id/nutritionWidget.json`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Recipe Nutrition](https://spoonacular.com/food-api/docs#Nutrition-by-ID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Spoonacular recipe ID. |
