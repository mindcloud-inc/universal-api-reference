# Create Customer with WooCommerce

Creates a new customer in WooCommerce.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [Create Customer](https://woocommerce.github.io/woocommerce-rest-api-docs/#create-a-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Customer email address. |
| `first_name` | body | `string` | no | Customer first name. |
| `last_name` | body | `string` | no | Customer last name. |
| `username` | body | `string` | no | Customer username. |
| `password` | body | `string` | no | Customer password. |
| `billing` | body | `object` | no | — |
| `billing.first_name` | body | `string` | no | — |
| `billing.last_name` | body | `string` | no | — |
| `meta_data[]` | body | `array` | no | — |
| `billing.company` | body | `string` | no | — |
| `billing.address_1` | body | `string` | no | — |
| `billing.address_2` | body | `string` | no | — |
| `billing.city` | body | `string` | no | — |
| `billing.state` | body | `string` | no | — |
| `billing.postcode` | body | `string` | no | — |
| `billing.country` | body | `string` | no | — |
| `billing.email` | body | `string` | no | — |
| `billing.phone` | body | `string` | no | — |
| `shipping` | body | `object` | no | — |
| `shipping.first_name` | body | `string` | no | — |
| `shipping.last_name` | body | `string` | no | — |
| `shipping.company` | body | `string` | no | — |
| `shipping.address_1` | body | `string` | no | — |
| `shipping.address_2` | body | `string` | no | — |
| `shipping.city` | body | `string` | no | — |
| `shipping.state` | body | `string` | no | — |
| `shipping.postcode` | body | `string` | no | — |
| `shipping.country` | body | `string` | no | — |
