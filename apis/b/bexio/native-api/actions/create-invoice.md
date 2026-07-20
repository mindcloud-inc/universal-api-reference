# Create Invoice with Bexio

Creates an invoice in Bexio.

## Endpoint

- **Method:** `POST`
- **Path:** `/2.0/kb_invoice`
- **Base URL:** `https://api.bexio.com`
- **Official documentation:** [Create Invoice](https://docs.bexio.com/#tag/Invoices/operation/v2CreateInvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `string` | no | Invoice position amount. |
| `document_nr` | body | `string` | no | Can not be used if automatic numbering is activated in frontend settings. Required if automatic numbering is deactivated. |
| `text` | body | `string` | no | Invoice position text. |
| `type` | body | `string` | no | Invoice position type. |
| `unit_price` | body | `string` | no | Invoice position unit price. |
| `title` | body | `string` | no | The invoice title. |
| `contact_id` | body | `number` | no | References a contact object. |
| `contact_sub_id` | body | `number` | no | References a contact object. |
| `user_id` | body | `number` | no | References a user object. |
| `pr_project_id` | body | `number` | no | References a project object. |
| `logopaper_id` | body | `number` | no | The logopaper ID. |
| `language_id` | body | `number` | no | References a language object. |
| `bank_account_id` | body | `number` | no | References a bank account object. |
| `currency_id` | body | `number` | no | References a currency object. |
| `payment_type_id` | body | `number` | no | References a payment type object. |
| `header` | body | `string` | no | The invoice header text. |
| `footer` | body | `string` | no | The invoice footer text. |
| `mwst_type` | body | `number` | no | Tax calculation mode for the invoice. |
| `mwst_is_net` | body | `boolean` | no | Whether taxes should be added to the total when mwst_type is 0. |
| `show_position_taxes` | body | `boolean` | no | Whether to show taxes for each position. |
| `is_valid_from` | body | `date` | no | The date from which the invoice is valid. |
| `is_valid_to` | body | `date` | no | The date until which the invoice is valid. |
| `contact_address_manual` | body | `string` | no | Use a custom invoice address instead of the contact invoice address. |
| `reference` | body | `string` | no | The invoice reference. |
| `api_reference` | body | `string` | no | Reference value for other systems. |
| `template_slug` | body | `string` | no | References a document template slug. |
| `positions[]` | body | `array<object>` | no | Invoice positions payload. |
