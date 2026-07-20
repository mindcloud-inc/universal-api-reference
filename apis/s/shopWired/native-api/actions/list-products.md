# List products with ShopWired

Retrieves products from ShopWired.

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://api.ecommerceapi.uk/v1`
- **Official documentation:** [List products](https://shopwired.readme.io/reference/listproducts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `number` | no | Return active products with 1 or inactive products with 0. Omit to return both. |
