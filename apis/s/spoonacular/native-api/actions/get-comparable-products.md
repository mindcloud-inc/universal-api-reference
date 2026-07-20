# Get Comparable Products with Spoonacular

Retrieves comparable grocery products from Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/products/upc/{upc}/comparable`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Comparable Products](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `upc` | path | `string` | yes | Required by the Spoonacular endpoint. |
