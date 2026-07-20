# Delete Offer Code with Gumroad

Deletes an existing offer code from Gumroad.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/products/:product_id/offer_codes/:id`
- **Base URL:** `https://api.gumroad.com/v2`
- **Official documentation:** [Delete Offer Code](https://gumroad.com/api#delete-/products/:product_id/offer_codes/:id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | The product ID. |
| `id` | path | `string` | yes | The offer code ID. |
