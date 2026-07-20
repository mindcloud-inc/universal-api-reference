# Update Category with Voog

Updates an existing category in the current Voog store.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ecommerce/v1/categories/:categoryId`
- **Base URL:** `{siteUrl}/admin/api`
- **Official documentation:** [Update Category](https://www.voog.com/developers/api/ecommerce/categories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category.name` | body | `string` | yes | Updated category name. |
| `category.slug` | body | `string` | yes | Updated category slug. |
| `categoryId` | path | `number` | yes | Numeric category ID. |
