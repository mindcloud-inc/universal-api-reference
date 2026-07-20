# Update Product Variant with SquareSpace

Updates a product variant in Squarespace.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/commerce/products/:productId/variants/:variantId`
- **Base URL:** `https://api.squarespace.com`
- **Official documentation:** [Update Product Variant](https://developers.squarespace.com/commerce-apis/products#update-product-variant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `list<string>` | yes | Product ID. |
| `variantId` | path | `list<string>` | yes | Variant ID. |
