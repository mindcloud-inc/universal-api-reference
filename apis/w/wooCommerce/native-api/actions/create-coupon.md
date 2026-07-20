# Create Coupon with WooCommerce

Creates a new coupon in WooCommerce.

## Endpoint

- **Method:** `POST`
- **Path:** `/coupons`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [Create Coupon](https://woocommerce.github.io/woocommerce-rest-api-docs/#create-a-coupon)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | Coupon code string. |
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
