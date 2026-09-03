# List Prices with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `prices`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [List Prices](https://docs.stripe.com/api/prices/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `boolean` | no | — |
| `currency` | query | `string` | no | — |
| `product` | query | `string` | no | — |
| `type` | query | `list` | no | Accepted values: `0`, `1`. |
