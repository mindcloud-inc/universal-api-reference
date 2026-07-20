# Create Customer with GoTeamup

Creates a new customer in GoTeamup.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers`
- **Base URL:** `https://goteamup.com/api/v2`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | Customer first name |
| `last_name` | body | `string` | yes | Customer last name |
| `email` | body | `string` | yes | Customer email address |
