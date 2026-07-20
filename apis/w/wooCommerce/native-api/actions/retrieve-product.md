# Retrieve Product with WooCommerce

Retrieves a product from WooCommerce.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/:id`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [Retrieve Product](https://woocommerce.github.io/woocommerce-rest-api-docs/#retrieve-a-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<number>` | yes | Unique numeric ID of the product to retrieve. |
