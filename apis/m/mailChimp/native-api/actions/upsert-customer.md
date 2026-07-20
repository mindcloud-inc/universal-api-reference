# Upsert Customer with Mailchimp

Creates or updates a customer in a Mailchimp e-commerce store.

## Endpoint

- **Method:** `PUT`
- **Path:** `ecommerce/stores/:store_id/customers/:customer_id`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Upsert Customer](https://mailchimp.com/developer/marketing/api/ecommerce-customers/add-or-update-customer/)

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
| `id` | body | `string` | yes | — |
| `sms_phone_number` | body | `string` | no | — |
| `store_id` | path | `string` | yes | The store id. |
| `customer_id` | path | `string` | yes | The customer id. |
| `email_address` | body | `string` | yes | The customer's email address. |
| `opt_in_status` | body | `boolean` | no | Whether the customer has opted in to email marketing. |
| `first_name` | body | `string` | no | Customer first name. |
| `last_name` | body | `string` | no | Customer last name. |
