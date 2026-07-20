# Create Order Note with WooCommerce

Creates an order note in WooCommerce.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/:id/notes`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [Create Order Note](https://woocommerce.github.io/woocommerce-rest-api-docs/#update-an-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<number>` | yes | Unique numeric ID of the order to update. |
| `note` | body | `string` | no | — |
