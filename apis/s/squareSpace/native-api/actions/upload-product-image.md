# Upload Product Image with SquareSpace

Uploads a product image to Squarespace.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/commerce/products/:id/images`
- **Base URL:** `https://api.squarespace.com`
- **Official documentation:** [Upload Product Image](https://developers.squarespace.com/commerce-apis/products#upload-product-image)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Image file binary payload. |
| `id` | path | `list<string>` | yes | Product ID. |
