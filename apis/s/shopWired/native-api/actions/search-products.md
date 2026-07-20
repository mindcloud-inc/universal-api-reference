# Search products with ShopWired

Finds products in ShopWired by keyword.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/search`
- **Base URL:** `https://api.ecommerceapi.uk/v1`
- **Official documentation:** [Search products](https://shopwired.readme.io/reference/searchproducts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keywords` | query | `string` | no | Keyword to search for. |
| `session_id` | query | `number` | no | Used to make sure the search engine returns the same results in subsequent calls. |
