# Recipe Taste by ID Image with Spoonacular

Retrieves a recipe taste image from Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/{id}/tasteWidget.png`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Recipe Taste by ID Image](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Required by the Spoonacular endpoint. |
