# Batch Products with Quizell

Creates multiple products in Quizell.

## Endpoint

- **Method:** `POST`
- **Path:** `/products/batch`
- **Base URL:** `https://api.quizell.com/api/v1`
- **Official documentation:** [Batch Products](https://docs.quizell.com/product-apis#post-multiple-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `products` | body | `object` | yes | Array of product objects. |
