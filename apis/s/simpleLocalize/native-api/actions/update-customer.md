# Update Customer with SimpleLocalize

Updates an existing customer in SimpleLocalize.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/customers/{customerKey}`
- **Base URL:** `https://api.simplelocalize.io`
- **Official documentation:** [Update Customer](https://api.simplelocalize.io/openapi/ui#/Customers/updateCustomer)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerKey` | path | `string` | yes |
| `key` | body | `string` | no |
| `displayName` | body | `string` | no |
| `description` | body | `string` | no |
