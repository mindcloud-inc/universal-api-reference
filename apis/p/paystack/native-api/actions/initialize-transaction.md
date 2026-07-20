# Initialize Transaction with Paystack

## Endpoint

- **Method:** `POST`
- **Path:** `/transaction/initialize`
- **Base URL:** `https://api.paystack.co`
- **Official documentation:** [Initialize Transaction](https://paystack.com/docs/api/transaction/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `amount` | body | `number` | yes |
| `currency` | body | `string` | no |
| `reference` | body | `string` | no |
