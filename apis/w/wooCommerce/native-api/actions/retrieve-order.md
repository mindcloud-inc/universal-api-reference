# Retrieve Order with WooCommerce

Retrieves an order from WooCommerce.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/:id`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [Retrieve Order](https://woocommerce.github.io/woocommerce-rest-api-docs/#retrieve-an-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<number>` | yes | Unique numeric ID of the order to retrieve. |
