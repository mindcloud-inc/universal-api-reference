# Get Product with Goody

Retrieves a specific product from Goody.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/products/:id`
- **Base URL:** `https://api.ongoody.com`
- **Official documentation:** [Get Product](https://developer.ongoody.com/api-reference/products/retrieve-a-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Product ID |
| `use_custom_catalog` | query | `boolean` | no | Limit to custom catalog only (for approved API partners) |
