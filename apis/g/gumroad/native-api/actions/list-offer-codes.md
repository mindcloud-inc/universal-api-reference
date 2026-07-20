# List Offer Codes with Gumroad

Retrieves offer codes for a Gumroad product.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/:product_id/offer_codes`
- **Base URL:** `https://api.gumroad.com/v2`
- **Official documentation:** [List Offer Codes](https://gumroad.com/api#get-/products/:product_id/offer_codes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | The product ID. |
