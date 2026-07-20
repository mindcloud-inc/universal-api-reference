# Update Order Status with Emporix Commerce Engine

Updates a sales order status in Emporix Commerce Engine.

## Endpoint

- **Method:** `POST`
- **Path:** `/order-v2/{tenantId}/salesorders/:orderId/transitions`
- **Base URL:** `https://api.emporix.io`
- **Official documentation:** [Update Order Status](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/orders/order/api-reference/api.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | The unique ID of the sales order whose status should be updated. |
