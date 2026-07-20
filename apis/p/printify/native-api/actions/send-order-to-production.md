# Send Order To Production with Printify

Sends an order to production in Printify.

## Endpoint

- **Method:** `POST`
- **Path:** `/shops/:shop_id/orders/:order_id/send_to_production.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Send Order To Production](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `string` | yes | Printify order id. |
| `shop_id` | path | `number` | yes | Printify shop id. |
