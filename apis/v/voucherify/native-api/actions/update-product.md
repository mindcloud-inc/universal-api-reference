# Update Product with Voucherify

Updates an existing product in Voucherify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/products/:productId`
- **Base URL:** `https://us1.api.voucherify.io/v1`
- **Official documentation:** [Update Product](https://docs.voucherify.io/reference/update-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `string` | yes | Voucherify product identifier. |
| `name` | body | `string` | no | Updated display name for the product. |
| `price` | body | `number` | no | Updated product price in minor currency units. |
