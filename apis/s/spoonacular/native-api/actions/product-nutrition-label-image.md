# Product Nutrition Label Image with Spoonacular

Retrieves a product nutrition label image from Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/products/{id}/nutritionLabel.png`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Product Nutrition Label Image](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Required by the Spoonacular endpoint. |
