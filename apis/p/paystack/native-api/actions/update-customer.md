# Update Customer with Paystack

## Endpoint

- **Method:** `PUT`
- **Path:** `/customer/:customerCode`
- **Base URL:** `https://api.paystack.co`
- **Official documentation:** [Update Customer](https://paystack.com/docs/api/customer/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerCode` | path | `string` | yes |
| `first_name` | body | `string` | no |
| `last_name` | body | `string` | no |
| `phone` | body | `string` | no |
| `metadata` | body | `object` | no |
