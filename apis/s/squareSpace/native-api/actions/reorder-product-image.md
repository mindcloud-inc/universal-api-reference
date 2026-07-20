# Reorder Product Image with SquareSpace

Updates product image order in Squarespace.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/commerce/products/:productId/images/:imageId/order`
- **Base URL:** `https://api.squarespace.com`
- **Official documentation:** [Reorder Product Image](https://developers.squarespace.com/commerce-apis/products#update-product-image-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageId` | path | `string` | yes | Image ID. |
| `productId` | path | `list<string>` | yes | Product ID. |
