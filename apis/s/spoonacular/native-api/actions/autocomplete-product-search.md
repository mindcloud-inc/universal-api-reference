# Autocomplete Product Search with Spoonacular

Autocompletes grocery products in Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/products/suggest`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Autocomplete Product Search](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Required by the Spoonacular endpoint. |
