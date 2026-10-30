# List Charges with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `charges`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [List Charges](https://docs.stripe.com/api/charges/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer` | query | `string` | no | — |
| `payment_intent` | query | `string` | no | — |
| `created` | query | `object` | no | Only return records created during this date interval. |
| `created[gt]` | query | `date` | no | After this date, exclusive. |
| `created[gte]` | query | `date` | no | On or after this date, inclusive. |
| `created[lt]` | query | `date` | no | Before this date, exclusive. |
| `created[lte]` | query | `date` | no | On or before this date, inclusive. |
