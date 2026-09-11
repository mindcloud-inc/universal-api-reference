# Get All Product Images with BigCommerce

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/catalog/products/:product_id/images`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | — |
| `include_fields` | query | `string` | no | Send multiple values as a array. |
