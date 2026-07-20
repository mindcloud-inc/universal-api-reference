# Retrieve Product Category with WooCommerce

Retrieves a product category from WooCommerce.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/categories/:id`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [Retrieve Product Category](https://woocommerce.github.io/woocommerce-rest-api-docs/#retrieve-a-product-category)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<number>` | yes | Unique numeric ID of the product category to retrieve. |
