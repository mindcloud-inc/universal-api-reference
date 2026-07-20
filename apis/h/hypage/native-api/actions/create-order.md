# Create Order with Hy.page

## Endpoint

- **Method:** `POST`
- **Path:** `/hyax-api/v1/orders`
- **Base URL:** `https://platform.hyax.com`
- **Official documentation:** [Create Order](https://platform.hyax.com/api-docs/order-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Person email; creates the person if new. |
| `notes` | body | `string` | no | Order notes. |
| `source` | body | `string` | no | Order source. |
| `amount` | body | `number` | yes | Order amount. |
| `currency` | body | `string` | no | Order currency. |
| `name` | body | `string` | no | Person name. |
| `orderId` | body | `string` | no | External order ID; used for deduplication if provided. |
| `isTest` | body | `boolean` | no | Whether the order is a test order. |
