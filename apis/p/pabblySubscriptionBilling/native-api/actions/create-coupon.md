# Create Coupon with Pabbly Subscription Billing

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/coupon/:productId`
- **Base URL:** `https://payments.pabbly.com/api`
- **Official documentation:** [Create Coupon](https://apidocs.pabbly.com/#423ee687-4e13-45a1-8b55-4be1ea86a47c)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `affiliate_id` | body | `string` | no |
| `apply_affiliate` | body | `string` | no |
| `apply_to` | body | `string` | no |
| `associate_plans` | body | `string` | no |
| `coupon_code` | body | `string` | no |
| `coupon_name` | body | `string` | no |
| `discount` | body | `string` | no |
| `discount_type` | body | `string` | no |
| `maximum_redemption` | body | `string` | no |
| `plans_array` | body | `string` | no |
| `product_id` | path | `string` | no |
| `redemption_cycle` | body | `string` | no |
| `redemption_type` | body | `string` | no |
| `valid_upto` | body | `string` | no |
