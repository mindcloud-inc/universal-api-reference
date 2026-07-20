# Create Customer with GorillaDesk

Creates a new customer in GorillaDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers`
- **Base URL:** `https://api.gorilladesk.com/v1`
- **Official documentation:** [Create Customer](https://api.gorilladesk.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_number` | body | `string` | no | — |
| `company` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `first_name` | body | `string` | yes | — |
| `last_name` | body | `string` | no | — |
| `location` | body | `object` | yes | Customer location object. |
| `location.address_line_1` | body | `string` | yes | — |
| `location.city` | body | `string` | yes | — |
| `location.state` | body | `string` | yes | — |
| `location.zip` | body | `string` | yes | — |
| `phones.phone` | body | `string` | no | — |
| `phones.type` | body | `string` | no | — |
| `phones[]` | body | `array<object>` | no | — |
| `status` | body | `string` | no | — |
