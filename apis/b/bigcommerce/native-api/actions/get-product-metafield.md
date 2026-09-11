# Get Product Metafield with BigCommerce

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/catalog/products/:productId/metafields/:metafieldId`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `productId` | path | `string` | yes |
| `metafieldId` | path | `string` | yes |
| `include_fields[]` | query | `array` | no |
| `exclude_fields[]` | query | `array` | no |
