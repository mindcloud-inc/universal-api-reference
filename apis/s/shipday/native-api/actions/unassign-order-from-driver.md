# Unassign Order from Driver with Shipday

Unassigns an existing order from a driver in Shipday.

## Endpoint

- **Method:** `PUT`
- **Path:** `/orders/unassign/:orderId`
- **Base URL:** `https://api.shipday.com`
- **Official documentation:** [Unassign Order from Driver](https://docs.shipday.com/reference/unassign-order-from-driver-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `number` | yes | Shipday order ID used in the request path. |
