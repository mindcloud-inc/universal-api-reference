# Get Category with Reloadify

Retrieves a category from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/categories/:category_id`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Get Category](https://app.reloadify.com/api-docs/index.html#/categories/getV2LanguagesLanguageIdCategoriesCategoryId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Language ID from the Reloadify language resource. |
| `category_id` | path | `string` | yes | Category ID. |
