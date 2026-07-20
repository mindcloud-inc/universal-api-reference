# Delete Product Image with SquareSpace

Deletes a product image from Squarespace.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/commerce/products/:productId/images/:imageId`
- **Base URL:** `https://api.squarespace.com`
- **Official documentation:** [Delete Product Image](https://developers.squarespace.com/commerce-apis/products#delete-one-product-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageId` | path | `string` | yes | Image ID. |
| `productId` | path | `list<string>` | yes | Product ID. |
