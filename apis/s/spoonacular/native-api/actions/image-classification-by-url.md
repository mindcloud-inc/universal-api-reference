# Image Classification by URL with Spoonacular

Classifies a food image URL with Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/images/classify`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Image Classification by URL](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageUrl` | query | `string` | yes | Required by the Spoonacular endpoint. |
