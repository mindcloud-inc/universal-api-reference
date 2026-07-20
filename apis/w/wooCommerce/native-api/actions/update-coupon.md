# Update Coupon with WooCommerce

Updates an existing coupon in WooCommerce.

## Endpoint

- **Method:** `PUT`
- **Path:** `/coupons/:id`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [Update Coupon](https://woocommerce.github.io/woocommerce-rest-api-docs/#update-a-coupon)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<number>` | yes | Unique numeric ID of the coupon to update. |
| `code` | body | `string` | no | Coupon code string. |
| `amount` | body | `string` | no | Discount amount as a string. |
| `discount_type` | body | `list<string>` | no | Coupon discount type such as percent, fixed_cart, or fixed_product. Accepted values: `fixed_cart`, `fixed_product`, `percent`. |
| `description` | body | `string` | no | Coupon description. |
| `date_expires` | body | `date` | no | Expiration date for the coupon. |
| `individual_use` | body | `boolean` | no | — |
| `exclude_sale_items` | body | `boolean` | no | — |
| `minimum_amount` | body | `string` | no | — |
| `maximum_amount` | body | `string` | no | — |
| `free_shipping` | body | `boolean` | no | — |
| `usage_limit` | body | `number` | no | — |
| `usage_limit_per_user` | body | `number` | no | — |
| `product_ids[]` | body | `array<number>` | no | — |
| `excluded_product_ids[]` | body | `array<number>` | no | — |
| `email_restrictions[]` | body | `array<string>` | no | — |
