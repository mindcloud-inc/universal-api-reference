# Create Customer with Voucherify

Creates a new customer in Voucherify, or updates an existing one.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers`
- **Base URL:** `https://us1.api.voucherify.io/v1`
- **Official documentation:** [Create Customer](https://docs.voucherify.io/reference/create-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | body | `string` | no | External customer identifier. |
| `name` | body | `string` | no | Customer display name. |
| `email` | body | `string` | no | Customer email address. |
