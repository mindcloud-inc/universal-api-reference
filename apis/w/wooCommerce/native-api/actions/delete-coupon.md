# Delete Coupon with WooCommerce

Deletes an existing coupon from WooCommerce.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/coupons/:id`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [Delete Coupon](https://woocommerce.github.io/woocommerce-rest-api-docs/#delete-a-coupon)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `force` | query | `boolean` | no | Whether to permanently delete the coupon. Defaults to false in WooCommerce. |
| `id` | path | `list<number>` | yes | Unique numeric ID of the coupon to delete. |
