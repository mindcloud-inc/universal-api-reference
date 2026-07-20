# Search Grocery Products with Spoonacular Food

Finds grocery products in Spoonacular Food by keyword.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/products/search`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Search Grocery Products](https://spoonacular.com/food-api/docs#Search-Grocery-Products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Grocery product search query. |
