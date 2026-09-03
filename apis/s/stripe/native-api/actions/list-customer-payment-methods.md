# List Customer Payment Methods with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `customers/:customer/payment_methods`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [List Customer Payment Methods](https://docs.stripe.com/api/payment_methods/customer_list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer` | path | `string` | yes | — |
| `type` | query | `string` | no | — |
| `allow_redisplay` | query | `list` | no | Accepted values: `0`, `1`, `2`. |
