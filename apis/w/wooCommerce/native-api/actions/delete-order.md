# Delete Order with WooCommerce

Deletes an existing order from WooCommerce.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/orders/:id`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [Delete Order](https://woocommerce.github.io/woocommerce-rest-api-docs/#delete-an-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `force` | query | `boolean` | no | Whether to permanently delete the order. Defaults to false in WooCommerce. |
| `id` | path | `list<number>` | yes | Unique numeric ID of the order to delete. |
