# Delete Product Variant with SquareSpace

Deletes a product variant from Squarespace.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/commerce/products/:productId/variants/:variantId`
- **Base URL:** `https://api.squarespace.com`
- **Official documentation:** [Delete Product Variant](https://developers.squarespace.com/commerce-apis/products#delete-one-product-variant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `list<string>` | yes | Product ID. |
| `variantId` | path | `list<string>` | yes | Variant ID. |
