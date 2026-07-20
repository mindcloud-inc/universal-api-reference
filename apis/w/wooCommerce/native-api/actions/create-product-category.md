# Create Product Category with WooCommerce

Creates a new product category in WooCommerce.

## Endpoint

- **Method:** `POST`
- **Path:** `/products/categories`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [Create Product Category](https://woocommerce.github.io/woocommerce-rest-api-docs/#create-a-product-category)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Category name. |
| `slug` | body | `string` | no | Category slug. |
| `description` | body | `string` | no | Category description. |
| `parent` | body | `list<number>` | no | Numeric ID of the parent category. |
| `display` | body | `list<string>` | no | Accepted values: `both`, `default`, `products`, `subcategories`. |
| `image` | body | `object` | no | — |
| `image.id` | body | `number` | no | — |
| `image.src` | body | `string` | no | — |
| `image.name` | body | `string` | no | — |
| `image.alt` | body | `string` | no | — |
| `menu_order` | body | `number` | no | — |
