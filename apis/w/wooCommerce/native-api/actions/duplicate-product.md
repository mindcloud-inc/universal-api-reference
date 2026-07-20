# Duplicate Product with WooCommerce

Creates a duplicate product in WooCommerce.

## Endpoint

- **Method:** `POST`
- **Path:** `/products/:productId/duplicate`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [Duplicate Product](https://woocommerce.github.io/woocommerce-rest-api-docs/#duplicate-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `list<number>` | yes | Unique numeric ID of the product to duplicate. |
