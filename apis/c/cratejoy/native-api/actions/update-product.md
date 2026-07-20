# Update Product with Cratejoy

Updates an existing product in Cratejoy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/products/:productId/`
- **Base URL:** `https://api.cratejoy.com`
- **Official documentation:** [Update Product](https://docs.cratejoy.com/reference/product-methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `number` | yes | The Cratejoy product ID. |
| `name` | body | `string` | no | The product name. |
| `ship_weight` | body | `number` | no | The product shipping weight. |
| `visible` | body | `boolean` | no | Whether the product is visible. |
