# List Category Products with Reloadify

Retrieves category products from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/categories/:category_id/products`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [List Category Products](https://app.reloadify.com/api-docs/index.html#/categories/getV2LanguagesLanguageIdCategoriesCategoryIdProducts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Language ID from the Reloadify language resource. |
| `category_id` | path | `string` | yes | Category ID. |
