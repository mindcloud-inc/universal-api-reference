# Add Custom Foods with Spoonacular

Creates a custom food in Spoonacular.

## Endpoint

- **Method:** `POST`
- **Path:** `/food/customFoods/add`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Add Custom Foods](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | yes | Required by the Spoonacular endpoint. |
| `requestBody` | body | `string` | yes | The required request body. |
| `username` | query | `string` | yes | Required by the Spoonacular endpoint. |
