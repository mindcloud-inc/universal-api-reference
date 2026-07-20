# Set Order Ready to Pickup with Shipday

Marks an existing order ready for pickup in Shipday.

## Endpoint

- **Method:** `PUT`
- **Path:** `/orders/:orderId/meta`
- **Base URL:** `https://api.shipday.com`
- **Official documentation:** [Set Order Ready to Pickup](https://docs.shipday.com/reference/order-ready-to-pickup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `number` | yes | Shipday order ID used in the request path. |
| `readyToPickup` | body | `boolean` | yes | Pickup-ready status sent in the request body. |
