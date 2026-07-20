# Create Product Variant with TrackMage

Creates a new product variant in TrackMage.

## Endpoint

- **Method:** `POST`
- **Path:** `/product_variants`
- **Base URL:** `https://api.trackmage.com/`
- **Official documentation:** [Create Product Variant](https://docs.trackmage.com/docs/product/product-variant.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | body | `string` | yes | The team reference to which the product variant belongs. |
| `sku` | body | `string` | yes | The SKU of product variant. |
| `imageUrl` | body | `string` | no | The URL of product variant image in the ecommerce store. |
| `product` | body | `string` | no | The [product](/docs/Product/product.html) reference to which the product variant belongs. |
| `price` | body | `string` | no | The price of product variant in the store currency. Default value is **0** |
| `externalSourceIntegration` | body | `string` | no | The workflow reference to integration for ecommerce store. |
| `externalSourceSyncId` | body | `string` | no | The id of the shipment in ecommerce store (WooCommerce, Shopify, etc.). |
