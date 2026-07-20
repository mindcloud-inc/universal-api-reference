# Update Customer with AdvantShop

Updates an existing customer in AdvantShop.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/{id}`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Update Customer](https://www.advantshop.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Customer identifier from AdvantShop. |
| `FirstName` | body | `string` | no | Updated customer first name. |
| `Email` | body | `string` | no | Updated customer email address. |
