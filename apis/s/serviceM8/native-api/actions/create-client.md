# Create Client with ServiceM8

## Endpoint

- **Method:** `POST`
- **Path:** `/api_1.0/company.json`
- **Base URL:** `https://api.servicem8.com`
- **Official documentation:** [Create Client](https://developer.servicem8.com/reference/createclients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Company name. Maximum length: 100. |
| `website` | body | `string` | no | Website URL. |
| `address` | body | `string` | no | Primary address. Maximum length: 500. |
| `address_street` | body | `string` | no | Street address. Maximum length: 500. |
| `address_city` | body | `string` | no | Address city. |
| `address_state` | body | `string` | no | Address state. |
| `address_postcode` | body | `string` | no | Address postcode. |
| `address_country` | body | `string` | no | Address country. |
| `billing_address` | body | `string` | no | Billing address. Maximum length: 500. |
| `billing_attention` | body | `string` | no | Billing attention line. |
| `payment_terms` | body | `string` | no | Payment terms. |
| `abn_number` | body | `string` | no | Australian Business Number. |
| `fax_number` | body | `string` | no | Fax number. |
| `tax_rate_uuid` | body | `string` | no | Tax rate UUID. |
| `parent_company_uuid` | body | `string` | no | Parent company UUID for site records. |
| `badges` | body | `string` | no | JSON array of badge UUIDs. |
| `uuid` | body | `string` | no | Optional record UUID. |
