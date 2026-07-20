# Update Product with WooCommerce

Updates an existing product in WooCommerce.

## Endpoint

- **Method:** `PUT`
- **Path:** `/products/:id`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [Update Product](https://woocommerce.github.io/woocommerce-rest-api-docs/#update-a-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<number>` | yes | Unique numeric ID of the product to update. |
| `name` | body | `string` | no | Product name. |
| `type` | body | `list<string>` | no | Product type such as simple, grouped, external, or variable. Accepted values: `external`, `grouped`, `simple`, `variable`. |
| `regular_price` | body | `string` | no | Regular product price as a string amount. |
| `sale_price` | body | `string` | no | Sale price as a string amount. |
| `sku` | body | `string` | no | — |
| `description` | body | `string` | no | Full product description in text or HTML. |
| `short_description` | body | `string` | no | Short product description in text or HTML. |
| `virtual` | body | `boolean` | no | — |
| `downloadable` | body | `boolean` | no | — |
| `manage_stock` | body | `boolean` | no | — |
| `stock_quantity` | body | `number` | no | — |
| `status` | body | `list<string>` | no | Catalog status such as draft, pending, private, or publish. Accepted values: `draft`, `pending`, `private`, `publish`. |
| `categories[]` | body | `array<object>` | no | — |
| `categories[].id` | body | `number` | no | — |
| `images[]` | body | `array<object>` | no | — |
| `images[].id` | body | `number` | no | — |
| `images[].src` | body | `string` | no | — |
| `images[].name` | body | `string` | no | — |
| `images[].alt` | body | `string` | no | — |
