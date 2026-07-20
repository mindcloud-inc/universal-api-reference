# Create Client with Content Snare

Creates a client in Content Snare.

## Endpoint

- **Method:** `POST`
- **Path:** `/partner_api/v1/clients`
- **Base URL:** `https://api.contentsnare.com`
- **Official documentation:** [Create Client](https://api.contentsnare.com/partner_api/v1/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_companies[]` | body | `array<object>` | no | Client Companies. |
| `client_companies[].name` | body | `string` | no | Company name |
| `email` | body | `string` | yes | Contact email address |
| `full_name` | body | `string` | yes | Contact full name |
| `first_name` | body | `string` | no | Contact first name |
| `last_name` | body | `string` | no | Contact last name |
| `phone` | body | `string` | no | Phone number |
| `language_code` | body | `string` | no | Language code |
