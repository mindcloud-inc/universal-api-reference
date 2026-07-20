# Delete Multiple Products with Quizell

Deletes multiple products from Quizell.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/products/delete/multiple`
- **Base URL:** `https://api.quizell.com/api/v1`
- **Official documentation:** [Delete Multiple Products](https://docs.quizell.com/product-apis#delete-multiple-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes | Array of product IDs to delete. |
