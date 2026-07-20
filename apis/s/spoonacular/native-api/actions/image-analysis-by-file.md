# Image Analysis by File with Spoonacular

Analyzes a food image with Spoonacular.

## Endpoint

- **Method:** `POST`
- **Path:** `/food/images/analyze`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Image Analysis by File](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | query | `string` | yes | Required by the Spoonacular endpoint. |
