# Update Order Status with YouCan

Updates an order status in YouCan.

## Endpoint

- **Method:** `PUT`
- **Path:** `/orders/{id}/status/{context}`
- **Base URL:** `https://api.youcan.shop`
- **Official documentation:** [Update Order Status](https://developer.youcan.shop/store-admin/orders/update_status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `context` | path | `string` | yes | Use status, shipping, or payment. |
| `id` | path | `string` | yes | — |
