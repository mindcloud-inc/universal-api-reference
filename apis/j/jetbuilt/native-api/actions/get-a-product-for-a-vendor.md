# Get a product for a vendor with Jetbuilt

This endpoint retrieves a product for a vendor by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `product_databases/:databaseId/vendors/:vendorId/products/:productId`
- **Base URL:** `https://app.jetbuilt.com/api/`
- **Official documentation:** [Get a product for a vendor](https://api.jetbuilt.com/customers#get-a-product-for-a-vendor)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `databaseId` | path | `string` | no |
| `productId` | path | `string` | no |
| `vendorId` | path | `string` | no |
