# Update Client with Content Snare

Updates a client in Content Snare.

## Endpoint

- **Method:** `PUT`
- **Path:** `/partner_api/v1/clients/{id}`
- **Base URL:** `https://api.contentsnare.com`
- **Official documentation:** [Update Client](https://api.contentsnare.com/partner_api/v1/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Client ID. |
| `client_companies[]` | body | `array<object>` | no | Client Companies. |
| `client_companies[].name` | body | `string` | no | Company name |
| `email` | body | `string` | no | Contact email address |
| `full_name` | body | `string` | no | Contact full name |
| `first_name` | body | `string` | no | Contact first name |
| `last_name` | body | `string` | no | Contact last name |
| `phone` | body | `string` | no | Phone number |
| `language_code` | body | `string` | no | Language code |
