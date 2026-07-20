# Calculate Order Shipping with Printify

Calculates order shipping in Printify.

## Endpoint

- **Method:** `POST`
- **Path:** `/shops/:shop_id/orders/shipping.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Calculate Order Shipping](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address_to` | body | `object` | yes | Recipient address for shipping calculation. |
| `line_items` | body | `list<object>` | yes | Order line items for shipping calculation. |
| `shop_id` | path | `number` | yes | Printify shop id. |
