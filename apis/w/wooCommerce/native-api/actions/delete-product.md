# Delete Product with WooCommerce

Deletes an existing product from WooCommerce.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/products/:id`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [Delete Product](https://woocommerce.github.io/woocommerce-rest-api-docs/#delete-a-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `force` | query | `boolean` | no | Whether to permanently delete the product. Defaults to false in WooCommerce. |
| `id` | path | `list<number>` | yes | Unique numeric ID of the product to delete. |
