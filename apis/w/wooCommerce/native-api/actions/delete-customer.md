# Delete Customer with WooCommerce

Deletes an existing customer from WooCommerce.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/customers/:id`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [Delete Customer](https://woocommerce.github.io/woocommerce-rest-api-docs/#delete-a-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `force` | query | `boolean` | yes | Required to be true because customer deletion does not support trashing. |
| `id` | path | `list<number>` | yes | Unique numeric ID of the customer to delete. |
| `reassign` | query | `number` | no | User ID to reassign posts to when deleting a customer. |
