# Create Plan with Paystack

## Endpoint

- **Method:** `POST`
- **Path:** `/plan`
- **Base URL:** `https://api.paystack.co`
- **Official documentation:** [Create Plan](https://paystack.com/docs/api/plan/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `amount` | body | `number` | yes |
| `interval` | body | `string` | yes |
| `description` | body | `string` | no |
| `currency` | body | `string` | no |
