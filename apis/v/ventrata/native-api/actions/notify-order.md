# Notify Order with Ventrata

Sends notifications for an order in Ventrata.

## Endpoint

- **Method:** `POST`
- **Path:** `octo/orders/:orderId/notify`
- **Base URL:** `https://api.ventrata.com`
- **Official documentation:** [Notify Order](https://docs.ventrata.com/capabilities/cart#post-orders-orderid-notify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | Order identifier from Ventrata. |
