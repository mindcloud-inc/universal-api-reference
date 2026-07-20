# Create Product with TrackMage

Creates a new product in TrackMage.

## Endpoint

- **Method:** `POST`
- **Path:** `/products`
- **Base URL:** `https://api.trackmage.com/`
- **Official documentation:** [Create Product](https://docs.trackmage.com/docs/product/product.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | body | `string` | yes | The team reference to which the product belongs. |
| `name` | body | `string` | no | The name of product. |
| `sku` | body | `string` | no | The SKU of product. |
| `originUrl` | body | `string` | no | The URL of product in the ecommerce store. |
| `imageUrl` | body | `string` | no | The URL of product image in the ecommerce store. |
| `externalSourceIntegration` | body | `string` | no | The workflow reference to integration for ecommerce store. |
| `externalSourceSyncId` | body | `string` | no | The id of the shipment in ecommerce store (WooCommerce, Shopify, etc.). |
