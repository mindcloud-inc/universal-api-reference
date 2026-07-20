# Update Product with MailBluster

Updates an existing product in MailBluster.

## Endpoint

- **Method:** `PUT`
- **Path:** `/products/:productId`
- **Base URL:** `https://api.mailbluster.com/api`
- **Official documentation:** [Update Product](https://app.mailbluster.com/api-doc/products/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `string` | yes | Unique product ID to update. |
| `name` | body | `string` | yes | Updated product name. |
