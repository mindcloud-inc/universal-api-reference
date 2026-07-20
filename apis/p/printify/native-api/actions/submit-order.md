# Submit Order with Printify

Submits an order to Printify.

## Endpoint

- **Method:** `POST`
- **Path:** `/shops/:shop_id/orders.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Submit Order](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address_to` | body | `object` | yes | Recipient shipping address. |
| `line_items` | body | `list<object>` | yes | Order line items. |
| `shipping_method` | body | `number` | yes | Shipping method code. |
| `shop_id` | path | `number` | yes | Printify shop id. |
