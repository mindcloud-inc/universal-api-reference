# List Invoice Line Items with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `invoices/:invoice/lines`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [List Invoice Line Items](https://docs.stripe.com/api/invoice-line-item/retrieve)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `invoice` | path | `string` | yes |
