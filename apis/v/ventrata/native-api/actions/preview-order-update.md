# Preview Order Update with Ventrata

Previews an existing order update in Ventrata.

## Endpoint

- **Method:** `PATCH`
- **Path:** `octo/orders/:orderId/preview`
- **Base URL:** `https://api.ventrata.com`
- **Official documentation:** [Preview Order Update](https://docs.ventrata.com/capabilities/cart#patch-orders-orderid-preview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | Order identifier from Ventrata. |
