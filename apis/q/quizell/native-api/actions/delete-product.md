# Delete Product with Quizell

Deletes an existing product from Quizell.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/products/delete/single/:product_id`
- **Base URL:** `https://api.quizell.com/api/v1`
- **Official documentation:** [Delete Product](https://docs.quizell.com/product-apis#delete-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `number` | yes | The ID of the product to delete. |
