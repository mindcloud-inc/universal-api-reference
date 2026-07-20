# Publish Product with Printify

Publishes a product in Printify.

## Endpoint

- **Method:** `POST`
- **Path:** `/shops/:shop_id/products/:product_id/publish.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Publish Product](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `boolean` | yes | Publish the product description. |
| `images` | body | `boolean` | yes | Publish the product images. |
| `keyFeatures` | body | `boolean` | yes | Publish the product key features. |
| `product_id` | path | `string` | yes | Printify product id. |
| `shipping_template` | body | `boolean` | yes | Publish the shipping template. |
| `shop_id` | path | `number` | yes | Printify shop id. |
| `tags` | body | `boolean` | yes | Publish the product tags. |
| `title` | body | `boolean` | yes | Publish the product title. |
| `variants` | body | `boolean` | yes | Publish the product variants. |
