# Get Products with BigCommerce

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/catalog/products`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | query | `string` | no | — |
| `name` | query | `string` | no | — |
| `sku` | query | `string` | no | — |
| `mpn` | query | `string` | no | — |
| `upc` | query | `string` | no | — |
| `condition` | query | `string` | no | — |
| `include_fields` | query | `string` | no | Send multiple values as a string. |
| `include` | query | `string` | no | A comma-separated list of sub-resources to return with a product object. When you specify options or modifiers, results are limited to 10 per page. |
| `date_modified` | query | `string` | no | — |
