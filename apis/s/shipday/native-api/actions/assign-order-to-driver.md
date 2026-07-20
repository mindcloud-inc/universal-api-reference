# Assign Order to Driver with Shipday

Assigns an existing order to a driver in Shipday.

## Endpoint

- **Method:** `PUT`
- **Path:** `/orders/assign/:orderId/:carrierId`
- **Base URL:** `https://api.shipday.com`
- **Official documentation:** [Assign Order to Driver](https://docs.shipday.com/reference/assign-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `number` | yes | Shipday order ID used in the request path. |
| `carrierId` | path | `number` | yes | Shipday carrier ID used in the request path. |
