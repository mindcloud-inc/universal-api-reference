# Create Category with Voog

Creates a new category in the current Voog store.

## Endpoint

- **Method:** `POST`
- **Path:** `/ecommerce/v1/categories`
- **Base URL:** `{siteUrl}/admin/api`
- **Official documentation:** [Create Category](https://www.voog.com/developers/api/ecommerce/categories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category.name` | body | `string` | yes | Category name. |
| `category.slug` | body | `string` | yes | Category slug. |
