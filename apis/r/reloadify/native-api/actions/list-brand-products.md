# List Brand Products with Reloadify

Retrieves products for a brand in Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/brands/:brand_id/products`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [List Brand Products](https://app.reloadify.com/api-docs/index.html#/brands/getV2LanguagesLanguageIdBrandsBrandIdProducts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `brand_id` | path | `string` | yes | Brand identifier. |
