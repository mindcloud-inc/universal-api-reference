# Create Product with SWELLEnterprise

Creates a new product in SWELLEnterprise.

## Endpoint

- **Method:** `POST`
- **Path:** `/products/products`
- **Base URL:** `https://dashboard.swellsystem.com/api/v1`
- **Official documentation:** [Create Product](https://dashboard.swellsystem.com/docs#products-POSTapi-v1-products-products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The product name. |
| `price` | body | `number` | yes | The product price. |
| `description` | body | `string` | no | The product description. |
| `billing_frequency` | body | `string` | no | The billing frequency. |
