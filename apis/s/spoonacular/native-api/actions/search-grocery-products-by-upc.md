# Search Grocery Products by UPC with Spoonacular

Retrieves a grocery product by UPC from Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/products/upc/{upc}`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Search Grocery Products by UPC](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `upc` | path | `string` | yes | Required by the Spoonacular endpoint. |
