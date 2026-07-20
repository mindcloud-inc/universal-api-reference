# Update Plan with Paystack

## Endpoint

- **Method:** `PUT`
- **Path:** `/plan/:planIdOrCode`
- **Base URL:** `https://api.paystack.co`
- **Official documentation:** [Update Plan](https://paystack.com/docs/api/plan/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `planIdOrCode` | path | `string` | yes |
| `name` | body | `string` | no |
| `amount` | body | `number` | no |
| `interval` | body | `string` | no |
| `description` | body | `string` | no |
| `currency` | body | `string` | no |
