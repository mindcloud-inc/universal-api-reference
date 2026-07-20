# Get Image Processing Status with SquareSpace

Retrieves product image processing status from Squarespace.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/commerce/products/:productId/images/:imageId/status`
- **Base URL:** `https://api.squarespace.com`
- **Official documentation:** [Get Image Processing Status](https://developers.squarespace.com/commerce-apis/products#get-image-processing-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageId` | path | `string` | yes | Image ID. |
| `productId` | path | `list<string>` | yes | Product ID. |
