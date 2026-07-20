# Update Customer with Stax

Updates a customer in Stax.

## Endpoint

- **Method:** `PUT`
- **Path:** `/customer/:id`
- **Base URL:** `https://apiprod.fattlabs.com`
- **Official documentation:** [Update Customer](https://docs.staxpayments.com/reference/update-customer-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Customer email |
| `firstname` | body | `string` | no | Customer first name |
| `id` | path | `string` | no | Customer identifier |
| `lastname` | body | `string` | no | Customer last name |
