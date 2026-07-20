# Assign Product Image to Variant with SquareSpace

Updates a product variant image in Squarespace.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/commerce/products/:productId/variants/:variantId/image`
- **Base URL:** `https://api.squarespace.com`
- **Official documentation:** [Assign Product Image to Variant](https://developers.squarespace.com/commerce-apis/products#associate-variant-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `list<string>` | yes | Product ID. |
| `variantId` | path | `list<string>` | yes | Variant ID. |
