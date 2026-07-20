# Update Offer Code with Gumroad

Updates an existing offer code in Gumroad.

## Endpoint

- **Method:** `PUT`
- **Path:** `/products/:product_id/offer_codes/:id`
- **Base URL:** `https://api.gumroad.com/v2`
- **Official documentation:** [Update Offer Code](https://gumroad.com/api#put-/products/:product_id/offer_codes/:id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | The product ID. |
| `id` | path | `string` | yes | The offer code ID. |
| `offer_code` | body | `string` | no | The offer code name. |
| `max_purchase_count` | body | `number` | no | The maximum number of redemptions allowed. |
