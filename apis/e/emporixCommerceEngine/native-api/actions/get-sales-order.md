# Get Sales Order with Emporix Commerce Engine

Retrieves a sales order from Emporix Commerce Engine.

## Endpoint

- **Method:** `GET`
- **Path:** `/order-v2/{tenantId}/salesorders/:orderId`
- **Base URL:** `https://api.emporix.io`
- **Official documentation:** [Get Sales Order](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/orders/order/api-reference/api.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | The unique ID of the sales order. |
