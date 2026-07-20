# Cancel Order with Printify

Cancels an unpaid order in Printify.

## Endpoint

- **Method:** `POST`
- **Path:** `/shops/:shop_id/orders/:order_id/cancel.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Cancel Order](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `string` | yes | Printify order id. |
| `shop_id` | path | `number` | yes | Printify shop id. |
