# Get Variant with Reloadify

Retrieves a product variant from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/variants/:variant_id`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Get Variant](https://app.reloadify.com/api-docs/index.html#/variants/getV2LanguagesLanguageIdVariantsVariantId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Language ID from the Reloadify language resource. |
| `variant_id` | path | `string` | yes | Variant ID. |
