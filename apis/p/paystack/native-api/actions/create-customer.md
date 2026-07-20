# Create Customer with Paystack

## Endpoint

- **Method:** `POST`
- **Path:** `/customer`
- **Base URL:** `https://api.paystack.co`
- **Official documentation:** [Create Customer](https://paystack.com/docs/api/customer/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `first_name` | body | `string` | no |
| `last_name` | body | `string` | no |
| `phone` | body | `string` | no |
| `metadata` | body | `object` | no |
