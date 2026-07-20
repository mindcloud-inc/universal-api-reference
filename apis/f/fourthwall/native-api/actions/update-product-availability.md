# Update Product Availability with Fourthwall

Updates a product's storefront availability in Fourthwall.

## Endpoint

- **Method:** `PUT`
- **Path:** `/open-api/v1.0/products/:productId/availability`
- **Base URL:** `https://api.fourthwall.com`
- **Official documentation:** [Update Product Availability](https://docs.fourthwall.com/api-reference/platform/products/update-product-availability)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `string` | yes | The product ID. |
| `available` | body | `boolean` | yes | Whether the product should be available for sale. |
