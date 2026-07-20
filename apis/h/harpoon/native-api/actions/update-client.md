# Update Client with Harpoon

Updates an existing client in Harpoon.

## Endpoint

- **Method:** `PUT`
- **Path:** `/clients/:id`
- **Base URL:** `https://app.harpoonapp.com/api`
- **Official documentation:** [Update Client](https://app.harpoonapp.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Client ID. |
| `client_name` | body | `string` | no | — |
| `source` | body | `string` | no | — |
| `address` | body | `string` | no | — |
| `tax_name` | body | `string` | no | — |
| `tax_number` | body | `string` | no | — |
| `language` | body | `string` | no | — |
| `contacts[]` | body | `array<object>` | no | — |
