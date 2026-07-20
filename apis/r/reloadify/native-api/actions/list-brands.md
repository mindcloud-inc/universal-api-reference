# List Brands with Reloadify

Retrieves brands from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/brands`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [List Brands](https://app.reloadify.com/api-docs/index.html#/brands/getV2LanguagesLanguageIdBrands)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_after` | query | `string` | no | Only include brands created after this timestamp. |
| `created_before` | query | `string` | no | Only include brands created before this timestamp. |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `updated_after` | query | `string` | no | Only include brands updated after this timestamp. |
| `updated_before` | query | `string` | no | Only include brands updated before this timestamp. |
