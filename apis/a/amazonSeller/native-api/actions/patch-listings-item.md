# Patch Listings Item with Amazon Seller

Updates an existing listings item in Amazon Seller.

## Endpoint

- **Method:** `PATCH`
- **Path:** `listings/2021-08-01/items/:sellerId/:sku`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Patch Listings Item](https://developer-docs.amazon.com/sp-api/reference/patchlistingsitem)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sellerId` | path | `string` | yes | — |
| `sku` | path | `string` | yes | — |
| `marketplaceIds` | query | `string<string>` | yes | — |
| `mode` | query | `string` | no | Set to `VALIDATION_PREVIEW` to validate the patch request without persisting listing changes. |
| `productType` | body | `string` | yes | — |
| `patches[]` | body | `array` | yes | — |
