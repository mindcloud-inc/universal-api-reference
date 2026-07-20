# Get Product with GetResponse

Retrieves a product by ID from a GetResponse shop.

## Endpoint

- **Method:** `GET`
- **Path:** `/shops/:shopId/products/:productId`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [Get Product](https://apireference.getresponse.com/#operation/getProductById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shopId` | path | `string` | yes | The shop ID |
| `productId` | path | `string` | yes | The product ID |
| `fields` | query | `string` | no | Comma-separated list of fields to return |
