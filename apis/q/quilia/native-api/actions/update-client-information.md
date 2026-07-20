# Update Client Information with Quilia

## Endpoint

- **Method:** `PATCH`
- **Path:** `clients/:id`
- **Base URL:** `https://api.quilia.dev/v2`
- **Official documentation:** [Update Client Information](https://api.quilia.dev/v2#tag/clients/PATCH/clients/%7Bid%7D)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address_1` | body | `string` | no | First line of the client's address |
| `address_2` | body | `string` | no | Second line of the client's address |
| `city` | body | `string` | no | The client's city |
| `country` | body | `string` | no | The client's country |
| `email` | body | `string` | no | The client's email address |
| `id` | path | `string` | yes | The unique identifier of the client to update |
| `language` | body | `string` | no | The client's preferred language |
| `name` | body | `string` | no | The client's full name |
| `phone` | body | `string` | no | The client's phone number |
| `postal_code` | body | `string` | no | The client's postal code |
| `state` | body | `string` | no | The client's state or province |
| `timezone` | body | `string` | no | The client's timezone |
| `date_of_birth` | body | `date` | no | The client's date of birth |
