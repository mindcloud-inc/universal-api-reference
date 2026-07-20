# Update Customer with Mailchimp

Updates an existing customer in a Mailchimp e-commerce store.

## Endpoint

- **Method:** `PATCH`
- **Path:** `ecommerce/stores/:store_id/customers/:customer_id`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Update Customer](https://mailchimp.com/developer/marketing/api/ecommerce-customers/update-customer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `object` | no | — |
| `address.address1` | body | `string` | no | — |
| `address.address2` | body | `string` | no | — |
| `address.city` | body | `string` | no | — |
| `address.country` | body | `string` | no | — |
| `address.country_code` | body | `string` | no | — |
| `address.postal_code` | body | `string` | no | — |
| `address.province` | body | `string` | no | — |
| `address.province_code` | body | `string` | no | — |
| `company` | body | `string` | no | — |
| `store_id` | path | `string` | yes | The store id. |
| `customer_id` | path | `string` | yes | The customer id. |
| `opt_in_status` | body | `boolean` | no | Whether the customer has opted in to email marketing. |
| `first_name` | body | `string` | no | Customer first name. |
| `last_name` | body | `string` | no | Customer last name. |
