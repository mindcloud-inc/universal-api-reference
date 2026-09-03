# List Credit Notes with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `credit_notes`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [List Credit Notes](https://docs.stripe.com/api/credit_notes/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer` | query | `string` | no |
| `invoice` | query | `string` | no |
