# Add Customer with Mailchimp

Creates a new customer in a Mailchimp e-commerce store.

## Endpoint

- **Method:** `POST`
- **Path:** `ecommerce/stores/:store_id/customers`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Add Customer](https://mailchimp.com/developer/marketing/api/ecommerce-customers/add-customer/)

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
| `first_name` | body | `string` | no | — |
| `last_name` | body | `string` | no | — |
| `sms_phone_number` | body | `string` | no | — |
| `store_id` | path | `string` | yes | The store id. |
| `id` | body | `string` | yes | A unique identifier for the customer in your system. |
| `email_address` | body | `string` | yes | The customer's email address. |
| `opt_in_status` | body | `boolean` | yes | Whether the customer has opted in to email marketing. |
