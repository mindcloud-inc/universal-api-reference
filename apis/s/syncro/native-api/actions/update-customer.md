# Update Customer with Syncro

Updates an existing customer in Syncro.

## Endpoint

- **Method:** `PUT`
- **Path:** `/customers/:id`
- **Base URL:** `https://mindcloud.syncromsp.com/api/v1`
- **Official documentation:** [Update Customer](https://api-docs.syncromsp.com/#/Customer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Syncro customer ID. |
| `business_name` | body | `string` | no | — |
| `firstname` | body | `string` | no | — |
| `lastname` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
| `mobile` | body | `string` | no | — |
| `address` | body | `string` | no | — |
| `address_2` | body | `string` | no | — |
| `city` | body | `string` | no | — |
| `state` | body | `string` | no | — |
| `zip` | body | `string` | no | — |
| `notes` | body | `string` | no | — |
| `get_sms` | body | `boolean` | no | — |
| `opt_out` | body | `boolean` | no | — |
| `no_email` | body | `boolean` | no | — |
| `get_billing` | body | `boolean` | no | — |
| `get_marketing` | body | `boolean` | no | — |
| `get_reports` | body | `boolean` | no | — |
| `ref_customer_id` | body | `number` | no | — |
| `referred_by` | body | `string` | no | — |
| `tax_rate_id` | body | `number` | no | — |
| `notification_email` | body | `string` | no | — |
| `invoice_cc_emails` | body | `string` | no | — |
| `invoice_term_id` | body | `number` | no | — |
| `properties` | body | `object` | no | — |
| `consent` | body | `object` | no | — |
