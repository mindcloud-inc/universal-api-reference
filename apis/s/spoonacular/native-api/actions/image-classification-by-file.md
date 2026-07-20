# Image Classification by File with Spoonacular

Classifies a food image with Spoonacular.

## Endpoint

- **Method:** `POST`
- **Path:** `/food/images/classify`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Image Classification by File](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | query | `string` | yes | Required by the Spoonacular endpoint. |
