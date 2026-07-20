# Delete Product with Printify

Deletes a product from Printify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/shops/:shop_id/products/:product_id.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Delete Product](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | Printify product id. |
| `shop_id` | path | `number` | yes | Printify shop id. |
