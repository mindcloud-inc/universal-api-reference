# Set Product Publish Succeeded with Printify

Marks a product publish as succeeded in Printify.

## Endpoint

- **Method:** `POST`
- **Path:** `/shops/:shop_id/products/:product_id/publishing_succeeded.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Set Product Publish Succeeded](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | Printify product id. |
| `shop_id` | path | `number` | yes | Printify shop id. |
| `external` | body | `object` | yes | External sales-channel product reference object with id and handle. |
