# Search Products with Ecwid

Finds products in Ecwid.

## Endpoint

- **Method:** `GET`
- **Path:** `/:storeId/products`
- **Base URL:** `https://app.ecwid.com/api/v3`
- **Official documentation:** [Search Products](https://docs.ecwid.com/api-reference/rest-api/products/search-products)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | query | `string` | no | Comma-separated Ecwid product IDs. |
| `sku` | query | `string` | no | — |
| `keyword` | query | `string` | no | — |
| `searchMethod` | query | `string` | no | One of STOREFRONT or CP. |
| `externalReferenceId` | query | `string` | no | — |
| `category` | query | `string` | no | — |
| `categories` | query | `string` | no | Comma-separated category IDs. |
| `includeProductsFromSubcategories` | query | `boolean` | no | — |
| `priceFrom` | query | `number` | no | — |
| `priceTo` | query | `number` | no | — |
| `createdFrom` | query | `date` | no | — |
| `createdTo` | query | `date` | no | — |
| `updatedFrom` | query | `date` | no | — |
| `updatedTo` | query | `date` | no | — |
| `enabled` | query | `boolean` | no | — |
| `inStock` | query | `boolean` | no | — |
| `visibleInStorefront` | query | `boolean` | no | — |
| `responseFields` | query | `string` | no | Limit the JSON response to selected fields. |
