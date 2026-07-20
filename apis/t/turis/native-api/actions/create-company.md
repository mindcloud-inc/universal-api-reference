# Create Company with Turis

Creates a new company in Turis.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/v1/companies`
- **Base URL:** `https://{tenant}.turis.app`
- **Official documentation:** [Create Company](https://documenter.getpostman.com/view/16452985/TzkyP1Er)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | no | Company street address. |
| `allow_users` | body | `string` | no | Whether buyers can be created for the company. |
| `city` | body | `string` | no | Company city. |
| `company_name` | body | `string` | no | Company name in Turis. |
| `company_reg_no` | body | `string` | no | Company registration number. |
| `company_slug` | body | `string` | no | Unique slug for the company. |
| `country_iso_code` | body | `string` | no | Two-letter country code for the company. |
| `currency_id` | body | `number` | yes | Currency identifier for the company. |
| `customer_no` | body | `string` | no | Customer number for the company. |
| `discount` | body | `string` | no | Company discount percentage. |
| `email` | body | `string` | no | Company email address. |
| `free_shipping_limit` | body | `string` | no | Free shipping threshold. |
| `language_id` | body | `string` | no | Company language identifier. |
| `order_confirmation_email` | body | `string` | no | Email for order confirmations. |
| `phone_number` | body | `string` | no | Company phone number. |
| `tz` | body | `string` | no | Company time zone. |
| `vat_number` | body | `string` | no | Company VAT number. |
| `website` | body | `string` | no | Company website. |
| `zip_code` | body | `string` | no | Company ZIP or postal code. |
