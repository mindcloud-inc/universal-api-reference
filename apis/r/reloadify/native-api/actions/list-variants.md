# List Variants with Reloadify

Retrieves product variants from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/variants`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [List Variants](https://app.reloadify.com/api-docs/index.html#/variants/getV2LanguagesLanguageIdVariants)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_after` | query | `string` | no | Only return variants created after this datetime. |
| `created_before` | query | `string` | no | Only return variants created before this datetime. |
| `language_id` | path | `string` | yes | Language ID from the Reloadify language resource. |
| `updated_after` | query | `string` | no | Only return variants updated after this datetime. |
| `updated_before` | query | `string` | no | Only return variants updated before this datetime. |
