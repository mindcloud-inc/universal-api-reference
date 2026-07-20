# Update Product Image with SquareSpace

Updates a product image in Squarespace.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/commerce/products/:productId/images/:imageId`
- **Base URL:** `https://api.squarespace.com`
- **Official documentation:** [Update Product Image](https://developers.squarespace.com/commerce-apis/products#update-product-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageId` | path | `string` | yes | Image ID. |
| `productId` | path | `list<string>` | yes | Product ID. |
