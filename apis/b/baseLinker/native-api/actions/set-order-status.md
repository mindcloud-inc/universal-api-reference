# Set Order Status with BaseLinker

Updates an order status in BaseLinker.

## Endpoint

- **Method:** `POST`
- **Path:** `/connector.php`
- **Base URL:** `https://api.baselinker.com`
- **Official documentation:** [Set Order Status](https://api.baselinker.com/index.php?method=setOrderStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | body | `number` | yes | Order identifier from the BaseLinker order manager. |
| `status_id` | body | `number` | yes | Status identifier to assign to the order. |
