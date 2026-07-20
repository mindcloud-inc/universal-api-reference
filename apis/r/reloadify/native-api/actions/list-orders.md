# List Orders with Reloadify

Retrieves orders from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/orders`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [List Orders](https://app.reloadify.com/api-docs/index.html#/orders/getV2LanguagesLanguageIdOrders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_after` | query | `string` | no | Only include orders created after this timestamp. |
| `created_before` | query | `string` | no | Only include orders created before this timestamp. |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `updated_after` | query | `string` | no | Only include orders updated after this timestamp. |
| `updated_before` | query | `string` | no | Only include orders updated before this timestamp. |
