# Create Or Update Variant with Reloadify

Creates or updates a product variant in Reloadify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/languages/:language_id/variants`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Create Or Update Variant](https://app.reloadify.com/api-docs/index.html#/variants/putV2LanguagesLanguageIdVariants)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Language ID from the Reloadify language resource. |
| `variant.id` | body | `string` | yes | Variant identifier. |
| `variant.product_id` | body | `string` | yes | Existing product ID for the variant. |
| `variant.title` | body | `string` | no | Variant title. |
