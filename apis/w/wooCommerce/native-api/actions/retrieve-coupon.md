# Retrieve Coupon with WooCommerce

Retrieves a coupon from WooCommerce.

## Endpoint

- **Method:** `GET`
- **Path:** `/coupons/:id`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [Retrieve Coupon](https://woocommerce.github.io/woocommerce-rest-api-docs/#retrieve-a-coupon)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<number>` | yes | Unique numeric ID of the coupon to retrieve. |
