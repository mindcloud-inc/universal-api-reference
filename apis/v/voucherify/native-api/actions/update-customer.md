# Update Customer with Voucherify

Updates an existing customer in Voucherify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/customers/:customerId`
- **Base URL:** `https://us1.api.voucherify.io/v1`
- **Official documentation:** [Update Customer](https://docs.voucherify.io/reference/update-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | Voucherify customer identifier. |
| `name` | body | `string` | no | Updated customer display name. |
| `email` | body | `string` | no | Updated customer email address. |
