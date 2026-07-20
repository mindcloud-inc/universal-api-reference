# List product reviews with ShopWired

Retrieves reviews for a product from ShopWired.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/{product_id}/reviews`
- **Base URL:** `https://api.ecommerceapi.uk/v1`
- **Official documentation:** [List product reviews](https://shopwired.readme.io/reference/listproductreviews)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `number` | yes | The unique identifier of the product. |
