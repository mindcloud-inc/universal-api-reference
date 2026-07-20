# Update Customer with GorillaDesk

Updates an existing customer in GorillaDesk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/customers/:customerId`
- **Base URL:** `https://api.gorilladesk.com/v1`
- **Official documentation:** [Update Customer](https://api.gorilladesk.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_number` | body | `string` | yes | — |
| `company` | body | `string` | no | — |
| `customerId` | path | `string` | yes | Customer Id |
| `email` | body | `string` | no | — |
| `first_name` | body | `string` | yes | — |
| `last_name` | body | `string` | no | — |
| `phones.phone` | body | `string` | no | — |
| `phones.type` | body | `string` | no | — |
| `phones[]` | body | `array<object>` | no | — |
| `status` | body | `string` | no | — |
