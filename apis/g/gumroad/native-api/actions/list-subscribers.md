# List Subscribers with Gumroad

Retrieves subscribers for a Gumroad product.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/:product_id/subscribers`
- **Base URL:** `https://api.gumroad.com/v2`
- **Official documentation:** [List Subscribers](https://gumroad.com/api#get-/products/:product_id/subscribers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | The product ID. |
| `email` | query | `string` | no | Filter subscribers by this email. |
| `paginated` | query | `boolean` | no | Set to true to limit the response and return a next page key. |
