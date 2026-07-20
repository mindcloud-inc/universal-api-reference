# Get Product GPSR with Printify

Retrieves a product's GPSR information from Printify.

## Endpoint

- **Method:** `GET`
- **Path:** `/shops/:shop_id/products/:product_id/gpsr.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Get Product GPSR](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | Printify product id. |
| `shop_id` | path | `number` | yes | Printify shop id. |
