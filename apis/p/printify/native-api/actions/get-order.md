# Get Order with Printify

Retrieves an order from Printify.

## Endpoint

- **Method:** `GET`
- **Path:** `/shops/:shop_id/orders/:order_id.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Get Order](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `string` | yes | Printify order id. |
| `shop_id` | path | `number` | yes | Printify shop id. |
