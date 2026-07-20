# List Shopping Carts with Reloadify

Retrieves shopping carts from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/shopping_carts`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [List Shopping Carts](https://app.reloadify.com/api-docs/index.html#/shopping_carts/getV2LanguagesLanguageIdShoppingCarts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_after` | query | `string` | no | Only include carts created after this timestamp. |
| `created_before` | query | `string` | no | Only include carts created before this timestamp. |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `updated_after` | query | `string` | no | Only include carts updated after this timestamp. |
| `updated_before` | query | `string` | no | Only include carts updated before this timestamp. |
