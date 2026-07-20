# Create Coupon with Payhip

Creates a new coupon in Payhip.

## Endpoint

- **Method:** `POST`
- **Path:** `/coupons`
- **Base URL:** `https://payhip.com/api/v2`
- **Official documentation:** [Create Coupon](https://payhip.com/api-reference/coupons/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `coupon_type` | body | `list` | yes | Choose whether the coupon applies to all products, specific products, or specific collections. Accepted values: `all_products`, `specific_collections`, `specific_products`. |
| `code` | body | `string` | yes | The coupon code customers will enter at checkout. |
| `percent_off` | body | `number` | no | Percentage discount to apply when using a percentage-based coupon. |
| `amount_off` | body | `number` | no | Fixed amount discount to apply when using an amount-based coupon. |
| `product_key` | body | `string` | no | Required when the coupon targets a specific product. |
| `collection_id` | body | `string` | no | Required when the coupon targets a specific collection. |
| `usage_limit` | body | `number` | no | Maximum number of times the coupon can be redeemed. |
| `minimum_purchase_amount` | body | `number` | no | Minimum purchase amount required before the coupon applies. |
| `start_date` | body | `string` | no | Optional start date for the coupon. |
| `end_date` | body | `string` | no | Optional end date for the coupon. |
| `notes` | body | `string` | no | Internal notes stored with the coupon. |
