# Create Or Update Brand with Reloadify

Creates or updates a brand in Reloadify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/languages/:language_id/brands`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Create Or Update Brand](https://app.reloadify.com/api-docs/index.html#/brands/putV2LanguagesLanguageIdBrands)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `brand.id` | body | `string` | yes | Brand identifier. |
| `brand.name` | body | `string` | yes | Brand name. |
