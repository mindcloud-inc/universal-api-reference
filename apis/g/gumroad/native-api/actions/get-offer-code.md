# Get Offer Code with Gumroad

Retrieves an offer code from Gumroad.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/:product_id/offer_codes/:id`
- **Base URL:** `https://api.gumroad.com/v2`
- **Official documentation:** [Get Offer Code](https://gumroad.com/api#get-/products/:product_id/offer_codes/:id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | The product ID. |
| `id` | path | `string` | yes | The offer code ID. |
