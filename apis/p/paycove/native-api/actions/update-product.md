# Update Product with Paycove

Updates a product in Paycove.

## Endpoint

- **Method:** `PATCH`
- **Path:** `products/:product_id`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [Update Product](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | Product ID. |
| `name` | body | `string` | no | Product name. |
| `description` | body | `string` | no | Product description. |
| `amount` | body | `number` | no | Product amount. |
| `currency` | body | `string` | no | Product currency. |
| `sales_tax` | body | `number` | no | Sales tax amount. |
| `custom_fields` | body | `object` | no | Custom product fields object. |
