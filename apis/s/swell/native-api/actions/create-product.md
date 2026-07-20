# Create Product with Swell

## Endpoint

- **Method:** `POST`
- **Path:** `/products`
- **Base URL:** `https://api.swell.store`
- **Official documentation:** [Create Product](https://developers.swell.is/backend-api/products/create-a-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The product name. |
| `price` | body | `number` | no | The product price. |
| `active` | body | `boolean` | no | Whether the product is active. |
| `options[]` | body | `array<object>` | no | Product option definitions. |
