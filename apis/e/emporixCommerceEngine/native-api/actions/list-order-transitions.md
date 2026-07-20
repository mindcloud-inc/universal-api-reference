# List Order Transitions with Emporix Commerce Engine

Retrieves sales order transitions from Emporix Commerce Engine.

## Endpoint

- **Method:** `GET`
- **Path:** `/order-v2/{tenantId}/salesorders/:orderId/transitions`
- **Base URL:** `https://api.emporix.io`
- **Official documentation:** [List Order Transitions](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/orders/order/api-reference/api.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | The unique ID of the sales order whose transitions should be listed. |
