# List Products with Reloadify

Retrieves products from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/products`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [List Products](https://app.reloadify.com/api-docs/index.html#/products/getV2LanguagesLanguageIdProducts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_after` | query | `string` | no | Only return products created after this datetime. |
| `created_before` | query | `string` | no | Only return products created before this datetime. |
| `language_id` | path | `string` | yes | Language ID from the Reloadify language resource. |
| `updated_after` | query | `string` | no | Only return products updated after this datetime. |
| `updated_before` | query | `string` | no | Only return products updated before this datetime. |
