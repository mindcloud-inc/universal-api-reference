# Recipe Nutrition Label Image with Spoonacular

Retrieves a recipe nutrition label image from Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/{id}/nutritionLabel.png`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Recipe Nutrition Label Image](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Required by the Spoonacular endpoint. |
