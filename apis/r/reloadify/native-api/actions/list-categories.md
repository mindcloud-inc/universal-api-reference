# List Categories with Reloadify

Retrieves categories from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/categories`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [List Categories](https://app.reloadify.com/api-docs/index.html#/categories/getV2LanguagesLanguageIdCategories)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_after` | query | `string` | no | Only return categories created after this datetime. |
| `created_before` | query | `string` | no | Only return categories created before this datetime. |
| `language_id` | path | `string` | yes | Language ID from the Reloadify language resource. |
| `updated_after` | query | `string` | no | Only return categories updated after this datetime. |
| `updated_before` | query | `string` | no | Only return categories updated before this datetime. |
