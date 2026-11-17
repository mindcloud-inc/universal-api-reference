# Update Customer with ECI Bolt

## Endpoint

- **Method:** `PATCH`
- **Path:** `/open/v1/customers/:id`
- **Base URL:** `https://app.bolttech.net`
- **Official documentation:** [Update Customer](https://app.bolttech.net/api-docs/index.html#/Customers/patch_open_v1_customers__id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Id of the customer. |
| `customer` | body | `object` | no | — |
| `customer.name` | body | `string` | no | Maximum length: 50. |
| `customer.status` | body | `string` | no | — |
| `customer.phone` | body | `string` | no | Maximum length: 11. |
| `customer.email` | body | `string` | no | — |
| `customer.notes` | body | `string` | no | — |
| `customer.po_required` | body | `boolean` | no | — |
| `customer.work_order_notes` | body | `string` | no | — |
| `customer.email_confirmation_to_supervisor` | body | `boolean` | no | — |
| `customer.opt_out_email_confirmation` | body | `boolean` | no | — |
| `customer.opt_out_auto_confirmation` | body | `boolean` | no | — |
| `customer.external_id` | body | `string` | no | — |
| `customer.corporate_address` | body | `object` | no | — |
| `customer.corporate_address.line1` | body | `string` | no | — |
| `customer.corporate_address.line2` | body | `string` | no | — |
| `customer.corporate_address.city` | body | `string` | no | — |
| `customer.corporate_address.state` | body | `string` | no | — |
| `customer.corporate_address.zip` | body | `string` | no | — |
| `customer.corporate_contact` | body | `object` | no | — |
| `customer.corporate_contact.first_name` | body | `string` | no | — |
| `customer.corporate_contact.last_name` | body | `string` | no | — |
| `customer.corporate_contact.email` | body | `string` | no | — |
| `customer.corporate_contact.phone` | body | `string` | no | Maximum length: 11. |
| `customer.corporate_contact.cellphone` | body | `string` | no | Maximum length: 11. |
| `customer.corporate_contact.fax` | body | `string` | no | Maximum length: 11. |
| `customer.billing_address` | body | `object` | no | — |
| `customer.billing_address.line1` | body | `string` | no | — |
| `customer.billing_address.line2` | body | `string` | no | — |
| `customer.billing_address.city` | body | `string` | no | — |
| `customer.billing_address.state` | body | `string` | no | — |
| `customer.billing_address.zip` | body | `string` | no | — |
| `customer.billing_contact` | body | `object` | no | — |
| `customer.billing_contact.first_name` | body | `string` | no | — |
| `customer.billing_contact.last_name` | body | `string` | no | — |
| `customer.billing_contact.email` | body | `string` | no | — |
| `customer.billing_contact.phone` | body | `string` | no | Maximum length: 11. |
| `customer.billing_contact.cellphone` | body | `string` | no | Maximum length: 11. |
| `customer.billing_contact.fax` | body | `string` | no | Maximum length: 11. |
| `etag` | body | `string` | yes | Use the etag returned by a fresh Get request to avoid overwriting a newer record. |
