# Confirm Order with Ventrata

Confirms an existing order in Ventrata.

## Endpoint

- **Method:** `POST`
- **Path:** `octo/orders/:orderId/confirm`
- **Base URL:** `https://api.ventrata.com`
- **Official documentation:** [Confirm Order](https://docs.ventrata.com/capabilities/cart#post-orders-orderid-confirm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | Order identifier from Ventrata. |
