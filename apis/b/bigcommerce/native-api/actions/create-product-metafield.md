# Create Product Metafield with BigCommerce

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/catalog/products/:productId/metafields`
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
| `key` | body | `string` | yes |
| `value` | body | `string` | yes |
| `namespace` | body | `string` | yes |
| `permission_set` | body | `list<string>` | yes |
| `description` | body | `string` | no |
