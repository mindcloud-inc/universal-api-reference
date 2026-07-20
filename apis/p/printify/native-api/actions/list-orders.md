# List Orders with Printify

Retrieves orders from a Printify shop.

## Endpoint

- **Method:** `GET`
- **Path:** `/shops/:shop_id/orders.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [List Orders](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of orders to return. |
| `page` | query | `number` | no | Result page to fetch. |
| `shop_id` | path | `number` | yes | Printify shop id. |
| `sku` | query | `string` | no | Filter orders by line item SKU. |
| `status` | query | `string` | no | Filter orders by status. |
