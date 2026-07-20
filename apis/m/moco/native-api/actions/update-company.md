# Update Company with Moco

## Endpoint

- **Method:** `PUT`
- **Path:** `/companies/:id`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [Update Company](https://everii-group.github.io/mocoapp-api-docs/sections/companies.html#put-companiesid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `address` | body | `string` | no |
| `alternative_correspondence_language` | body | `string` | no |
| `bank_bic` | body | `string` | no |
| `bank_owner` | body | `string` | no |
| `billing_email_cc` | body | `string` | no |
| `billing_notes` | body | `string` | no |
| `country_code` | body | `string` | no |
| `credit_number` | body | `string` | no |
| `currency` | body | `string` | no |
| `custom_properties` | body | `string` | no |
| `customer_tax` | body | `string` | no |
| `customer_vat_code_id` | body | `string` | no |
| `debit_number` | body | `string` | no |
| `default_invoice_due_days` | body | `string` | no |
| `default_payment_means` | body | `string` | no |
| `email` | body | `string` | no |
| `fax` | body | `string` | no |
| `footer` | body | `string` | no |
| `iban` | body | `string` | no |
| `id` | path | `number` | yes |
| `identifier` | body | `string` | no |
| `info` | body | `string` | no |
| `invoice_format` | body | `string` | no |
| `name` | body | `string` | no |
| `phone` | body | `string` | no |
| `supplier_tax` | body | `string` | no |
| `supplier_vat_code_id` | body | `string` | no |
| `tags` | body | `string` | no |
| `type` | body | `string` | no |
| `user_id` | body | `string` | no |
| `vat_identifier` | body | `string` | no |
| `website` | body | `string` | no |
