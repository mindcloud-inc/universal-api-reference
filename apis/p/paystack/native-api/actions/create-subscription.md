# Create Subscription with Paystack

## Endpoint

- **Method:** `POST`
- **Path:** `/subscription`
- **Base URL:** `https://api.paystack.co`
- **Official documentation:** [Create Subscription](https://paystack.com/docs/api/subscription/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer` | body | `string` | yes |
| `plan` | body | `string` | yes |
| `authorization` | body | `string` | yes |
