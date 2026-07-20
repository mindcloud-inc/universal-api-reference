# Update Address with Easyship

Updates an existing address in Easyship.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/addresses/:address_id`
- **Base URL:** `https://public-api.easyship.com/2024-09`
- **Official documentation:** [Update Address](https://developers.easyship.com/reference/addresses_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address_id` | path | `string` | yes | The Easyship address ID. |
| `line_1` | body | `string` | no | First address line. |
| `line_2` | body | `string` | no | Second address line. |
| `city` | body | `string` | no | Address city. |
| `state` | body | `string` | no | Address state or province. |
| `postal_code` | body | `string` | no | Address postal code. |
| `country_alpha2` | body | `string` | no | Two-letter country code. |
| `company_name` | body | `string` | no | Company name on the address. |
| `contact_name` | body | `string` | no | Contact full name. |
| `contact_email` | body | `string` | no | Contact email address. |
| `contact_phone` | body | `string` | no | Contact phone number. |
