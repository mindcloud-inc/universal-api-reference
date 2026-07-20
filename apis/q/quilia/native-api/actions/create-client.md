# Create Client with Quilia

## Endpoint

- **Method:** `POST`
- **Path:** `clients`
- **Base URL:** `https://api.quilia.dev/v2`
- **Official documentation:** [Create Client](https://api.quilia.dev/v2#tag/clients/POST/clients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address_1` | body | `string` | no | The first line of the address |
| `address_2` | body | `string` | no | The second line of the address |
| `city` | body | `string` | no | The city |
| `country` | body | `string` | no | The country |
| `email` | body | `string` | no | The email of the client |
| `language_code` | body | `string` | no | The language code of the client |
| `name` | body | `string` | yes | The name of the client |
| `name_first` | body | `string` | no | The first name of the client |
| `name_last` | body | `string` | no | The last name of the client |
| `postal_code` | body | `string` | no | The postal code |
| `state` | body | `string` | no | The state or province |
| `phone` | body | `string` | yes | The phone number of the client |
| `date_of_birth` | body | `date` | no | The date of birth in YYYY-MM-DD format |
