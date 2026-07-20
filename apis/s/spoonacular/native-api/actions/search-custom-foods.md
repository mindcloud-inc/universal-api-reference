# Search Custom Foods with Spoonacular

Searches custom foods in Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/customFoods/search`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Search Custom Foods](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | yes | Required by the Spoonacular endpoint. |
| `query` | query | `string` | yes | Required by the Spoonacular endpoint. |
| `username` | query | `string` | yes | Required by the Spoonacular endpoint. |
