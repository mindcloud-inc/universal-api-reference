# Create Product Variant Image with BigCommerce

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/catalog/products/:productId/variants/:variantId/image`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `productId` | path | `string` | yes |
| `variantId` | path | `string` | yes |
| `image_url` | body | `string` | yes |
