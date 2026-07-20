# Get Product Offers with SearchApi

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://www.searchapi.io/api/v1`
- **Official documentation:** [Get Product Offers](https://www.searchapi.io/docs/google-product-offers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | query | `string` | yes | Google Shopping product ID. |
| `product_token` | query | `string` | no | Google Shopping product token. Optional when Product ID is provided. |
