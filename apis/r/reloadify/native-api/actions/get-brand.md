# Get Brand with Reloadify

Retrieves a brand from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/brands/:brand_id`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Get Brand](https://app.reloadify.com/api-docs/index.html#/brands/getV2LanguagesLanguageIdBrandsBrandId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `brand_id` | path | `string` | yes | Brand identifier. |
