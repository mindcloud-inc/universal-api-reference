# Search Grocery Product by UPC with Spoonacular Food

Finds a grocery product in Spoonacular Food by UPC.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/products/upc/:upc`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Search Grocery Product by UPC](https://spoonacular.com/food-api/docs#Search-Grocery-Products-by-UPC)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `upc` | path | `string` | yes | The product UPC code. |
