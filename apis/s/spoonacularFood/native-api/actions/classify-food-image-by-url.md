# Classify Food Image by URL with Spoonacular Food

Classifies a food image in Spoonacular Food by URL.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/images/classify`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Classify Food Image by URL](https://spoonacular.com/food-api/docs#Image-Classification-by-URL)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageUrl` | query | `string` | yes | Public URL of the food image to classify. |
