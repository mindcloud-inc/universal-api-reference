# Set Product Publish Failed with Printify

Marks a product publish as failed in Printify.

## Endpoint

- **Method:** `POST`
- **Path:** `/shops/:shop_id/products/:product_id/publishing_failed.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Set Product Publish Failed](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | Printify product id. |
| `shop_id` | path | `number` | yes | Printify shop id. |
| `reason` | body | `string` | yes | Reason the product publish attempt failed. |
