# Get Order with Ecwid

Retrieves an order from Ecwid.

## Endpoint

- **Method:** `GET`
- **Path:** `/:storeId/orders/:orderId`
- **Base URL:** `https://app.ecwid.com/api/v3`
- **Official documentation:** [Get Order](https://docs.ecwid.com/api-reference/rest-api/orders/get-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `number` | yes | Ecwid order ID. |
