# Update Client with ServiceM8

## Endpoint

- **Method:** `POST`
- **Path:** `/api_1.0/company/:uuid.json`
- **Base URL:** `https://api.servicem8.com`
- **Official documentation:** [Update Client](https://developer.servicem8.com/reference/updateclients)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `uuid` | path | `string` | yes |
| `name` | body | `string` | no |
| `abn_number` | body | `string` | no |
| `address` | body | `string` | no |
| `billing_address` | body | `string` | no |
| `parent_company_uuid` | body | `string` | no |
| `website` | body | `string` | no |
| `address_street` | body | `string` | no |
| `address_city` | body | `string` | no |
| `address_state` | body | `string` | no |
| `address_postcode` | body | `string` | no |
| `address_country` | body | `string` | no |
| `fax_number` | body | `string` | no |
| `badges` | body | `string` | no |
| `tax_rate_uuid` | body | `string` | no |
| `billing_attention` | body | `string` | no |
| `payment_terms` | body | `string` | no |
