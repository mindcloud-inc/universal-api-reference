# Create Or Update Category with Reloadify

Creates or updates a category in Reloadify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/languages/:language_id/categories`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Create Or Update Category](https://app.reloadify.com/api-docs/index.html#/categories/putV2LanguagesLanguageIdCategories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Language ID from the Reloadify language resource. |
| `category.id` | body | `string` | yes | Category identifier. |
| `category.name` | body | `string` | yes | Category name. |
