# Create Product with Voucherify

Creates a new product in Voucherify, or updates an existing one.

## Endpoint

- **Method:** `POST`
- **Path:** `/products`
- **Base URL:** `https://us1.api.voucherify.io/v1`
- **Official documentation:** [Create Product](https://docs.voucherify.io/reference/create-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | body | `string` | no | External product identifier. |
| `name` | body | `string` | no | Display name for the product. |
| `price` | body | `number` | no | Product price in minor currency units. |
| `image_url` | body | `string` | no | Image URL for the product. |
