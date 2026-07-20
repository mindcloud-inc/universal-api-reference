# Delete Order with Shipday

Deletes an existing order from Shipday.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/orders/:orderId`
- **Base URL:** `https://api.shipday.com`
- **Official documentation:** [Delete Order](https://docs.shipday.com/reference/delete-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `number` | yes | Shipday order ID used in the request path. |
