# Create Customer with SimpleLocalize

Creates a new customer in SimpleLocalize.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/customers`
- **Base URL:** `https://api.simplelocalize.io`
- **Official documentation:** [Create Customer](https://api.simplelocalize.io/openapi/ui#/Customers/createCustomer)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `key` | body | `string` | yes |
| `displayName` | body | `string` | no |
| `description` | body | `string` | no |
