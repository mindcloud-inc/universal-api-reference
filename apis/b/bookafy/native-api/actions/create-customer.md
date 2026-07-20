# Create Customer with Bookafy

Creates a customer in Bookafy.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers`
- **Base URL:** `https://app.bookafy.com/api/v2`
- **Official documentation:** [Create Customer](https://app.bookafy.com/api-docs/v3/customers_part1.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer.name` | body | `string` | yes | Customer name. |
| `customer.email` | body | `string` | no | Customer email. |
| `customer.phone` | body | `string` | no | Customer phone. |
