# List Products with Printify

Retrieves products from a Printify shop.

## Endpoint

- **Method:** `GET`
- **Path:** `/shops/:shop_id/products.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [List Products](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of products to return. |
| `page` | query | `number` | no | Result page to fetch. |
| `shop_id` | path | `number` | yes | Printify shop id. |
