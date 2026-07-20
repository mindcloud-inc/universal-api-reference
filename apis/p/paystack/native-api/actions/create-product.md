# Create Product with Paystack

## Endpoint

- **Method:** `POST`
- **Path:** `/product`
- **Base URL:** `https://api.paystack.co`
- **Official documentation:** [Create Product](https://paystack.com/docs/api/product/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `description` | body | `string` | yes |
| `price` | body | `number` | yes |
| `currency` | body | `string` | no |
