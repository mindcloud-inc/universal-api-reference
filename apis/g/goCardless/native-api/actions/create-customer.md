# Create Customer with GoCardless

Creates a new customer in GoCardless.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [Create Customer](https://developer.gocardless.com/api-reference/#customers-create-a-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | — |
| `given_name` | body | `string` | no | — |
| `family_name` | body | `string` | no | — |
| `company_name` | body | `string` | no | — |
| `address_line1` | body | `string` | no | — |
| `address_line2` | body | `string` | no | — |
| `address_line3` | body | `string` | no | — |
| `city` | body | `string` | no | — |
| `postal_code` | body | `string` | no | — |
| `country_code` | body | `string` | no | — |
| `region` | body | `string` | no | — |
| `language` | body | `list` | no | Accepted values: `0`, `1`, `10`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `phone_number` | body | `string` | no | — |
| `danish_identity_number` | body | `string` | no | — |
| `swedish_identity_number` | body | `string` | no | — |
| `metadata` | body | `object` | no | — |
