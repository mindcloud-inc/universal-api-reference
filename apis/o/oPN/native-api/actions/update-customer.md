# Update Customer with OPN

Updates an existing customer in OPN.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/customers/:id`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [Update Customer](https://docs.omise.co/customer-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | The updated customer description. |
| `email` | body | `string` | no | The updated customer email address. |
| `id` | path | `string` | yes | The customer ID to update. |
