# Create Product with RAYNET CRM

## Endpoint

- **Method:** `PUT`
- **Path:** `product/`
- **Base URL:** `https://app.raynetcrm.com/api/v2/`
- **Official documentation:** [Create Product](https://app.raynetcrm.com/api/doc/index-en.html#tag/Products/operation/productInsert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | Product code. |
| `cost` | body | `number` | no | Product cost. |
| `description` | body | `string` | no | Product description. |
| `name` | body | `string` | yes | Product name. |
| `price` | body | `number` | no | Product base price. |
| `taxRate` | body | `number` | no | Product tax rate. |
| `unit` | body | `string` | no | Product unit. |
