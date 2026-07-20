# Unpublish Product with Printify

Unpublishes a product in Printify.

## Endpoint

- **Method:** `POST`
- **Path:** `/shops/:shop_id/products/:product_id/unpublish.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Unpublish Product](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | Printify product id. |
| `shop_id` | path | `number` | yes | Printify shop id. |
