# Update Customer with Bookafy

Updates a customer in Bookafy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/customers/:id`
- **Base URL:** `https://app.bookafy.com/api/v2`
- **Official documentation:** [Update Customer](https://app.bookafy.com/api-docs/v3/customers_part2.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Customer ID from Bookafy. |
| `customer.name` | body | `string` | yes | Customer name. |
| `customer.email` | body | `string` | no | Customer email. |
| `customer.phone` | body | `string` | no | Customer phone. |
