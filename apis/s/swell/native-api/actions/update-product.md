# Update Product with Swell

## Endpoint

- **Method:** `PUT`
- **Path:** `/products/:id`
- **Base URL:** `https://api.swell.store`
- **Official documentation:** [Update Product](https://developers.swell.is/backend-api/products/update-a-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Swell product ID. |
| `name` | body | `string` | no | The product name. |
| `price` | body | `number` | no | The product price. |
| `active` | body | `boolean` | no | Whether the product is active. |
| `options[]` | body | `array<object>` | no | Product option definitions. |
