# Retrieve Customer with WooCommerce

Retrieves a customer from WooCommerce.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/:id`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [Retrieve Customer](https://woocommerce.github.io/woocommerce-rest-api-docs/#retrieve-a-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<number>` | yes | Unique numeric ID of the customer to retrieve. |
