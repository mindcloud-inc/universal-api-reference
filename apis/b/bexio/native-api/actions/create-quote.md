# Create Quote with Bexio

Creates a quote in Bexio.

## Endpoint

- **Method:** `POST`
- **Path:** `/2.0/kb_offer`
- **Base URL:** `https://api.bexio.com`
- **Official documentation:** [Create Quote](https://docs.bexio.com/#tag/Quotes/operation/v2CreateQuote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `number` | no | Contact ID. |
| `user_id` | body | `number` | no | User ID. |
| `document_nr` | body | `string` | no | Quote document number. |
| `title` | body | `string` | no | Quote title. |
| `positions[]` | body | `array<object>` | no | Quote positions array. |
| `contact_sub_id` | body | `number` | no | Contact sub ID. |
| `pr_project_id` | body | `number` | no | Project ID. |
| `logopaper_id` | body | `number` | no | Logo paper ID. |
| `language_id` | body | `number` | no | Language ID. |
| `bank_account_id` | body | `number` | no | Bank account ID. |
| `currency_id` | body | `number` | no | Currency ID. |
| `payment_type_id` | body | `number` | no | Payment type ID. |
| `mwst_type` | body | `list<number>` | no | Tax type. Accepted values: `0`, `1`, `2`. |
| `mwst_is_net` | body | `boolean` | no | Whether taxes are added to the total. |
| `show_position_taxes` | body | `boolean` | no | Whether to show position taxes. |
| `is_valid_from` | body | `date` | no | Valid from date. |
| `is_valid_until` | body | `date` | no | Valid until date. |
| `contact_address_manual` | body | `string` | no | Manual contact address. |
| `delivery_address_type` | body | `list<number>` | no | Delivery address type. Accepted values: `0`, `1`. |
| `delivery_address_manual` | body | `string` | no | Manual delivery address. |
| `header` | body | `string` | no | Header text. |
| `footer` | body | `string` | no | Footer text. |
| `kb_terms_of_payment_template_id` | body | `number` | no | Terms of payment template ID. |
| `template_slug` | body | `string` | no | Document template slug. |
| `api_reference` | body | `string` | no | API-only external reference. |
| `viewed_by_client_at` | body | `string` | no | Viewed-by-client timestamp. |
