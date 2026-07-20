# Create Address with Easyship

Creates a new address in Easyship.

## Endpoint

- **Method:** `POST`
- **Path:** `/addresses`
- **Base URL:** `https://public-api.easyship.com/2024-09`
- **Official documentation:** [Create Address](https://developers.easyship.com/reference/addresses_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `line_1` | body | `string` | yes | First address line. |
| `line_2` | body | `string` | no | Second address line. |
| `city` | body | `string` | yes | Address city. |
| `state` | body | `string` | no | Address state or province. |
| `postal_code` | body | `string` | no | Address postal code. |
| `country_alpha2` | body | `string` | no | Two-letter country code. |
| `company_name` | body | `string` | yes | Company name on the address. |
| `contact_name` | body | `string` | yes | Contact full name. |
| `contact_email` | body | `string` | yes | Contact email address. |
| `contact_phone` | body | `string` | yes | Contact phone number. |
