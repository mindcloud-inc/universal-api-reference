# Create Purchase Order with Bexio

Creates a purchase order in Bexio.

## Endpoint

- **Method:** `POST`
- **Path:** `/3.0/purchase_orders`
- **Base URL:** `https://api.bexio.com`
- **Official documentation:** [Create Purchase Order](https://docs.bexio.com/#tag/Purchase-Orders/operation/v3PurchaseOrderCreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_nr` | body | `string` | no | — |
| `kb_payment_template_id` | body | `number` | no | — |
| `payment_type_id` | body | `number` | no | — |
| `title` | body | `string` | no | — |
| `contact_id` | body | `number` | no | — |
| `contact_sub_id` | body | `number` | no | — |
| `template_slug` | body | `string` | no | — |
| `user_id` | body | `number` | no | — |
| `project_id` | body | `number` | no | — |
| `logopaper_id` | body | `number` | no | — |
| `language_id` | body | `number` | no | — |
| `bank_account_id` | body | `number` | no | — |
| `currency_id` | body | `number` | no | — |
| `header` | body | `string` | no | — |
| `footer` | body | `string` | no | — |
| `mwst_type` | body | `list<string>` | no | Accepted values: `0`, `1`, `2`. |
| `mwst_is_net` | body | `boolean` | no | — |
| `is_compact_view` | body | `boolean` | no | — |
| `show_position_taxes` | body | `boolean` | no | — |
| `salesman_user_id` | body | `number` | no | — |
| `is_valid_from` | body | `date` | no | — |
| `is_valid_to` | body | `date` | no | — |
| `delivery_address_type` | body | `list<string>` | no | Accepted values: `0`, `1`. |
| `contact_address_manual` | body | `string` | no | — |
| `delivery_address_manual` | body | `string` | no | — |
| `nb_decimals_amount` | body | `number` | no | — |
| `nb_decimals_price` | body | `number` | no | — |
| `terms_of_payment_text` | body | `string` | no | — |
| `reference` | body | `string` | no | — |
| `api_reference` | body | `string` | no | — |
| `mail` | body | `string` | no | — |
| `positions` | body | `object` | no | — |
