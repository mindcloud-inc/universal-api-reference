# Create Offer Code with Gumroad

Creates a new offer code in Gumroad.

## Endpoint

- **Method:** `POST`
- **Path:** `/products/:product_id/offer_codes`
- **Base URL:** `https://api.gumroad.com/v2`
- **Official documentation:** [Create Offer Code](https://gumroad.com/api#post-/products/:product_id/offer_codes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | The product ID. |
| `name` | body | `string` | yes | The coupon code used at checkout. |
| `amount_off` | body | `number` | yes | The discount amount. |
| `offer_type` | body | `string` | no | Use cents or percent. |
| `max_purchase_count` | body | `number` | no | The maximum number of redemptions allowed. |
| `universal` | body | `boolean` | no | Whether the offer code applies to all products. |
