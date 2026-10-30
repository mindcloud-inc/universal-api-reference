# Get Balance Transactions with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `/balance_transactions`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Get Balance Transactions](https://docs.stripe.com/api/balance_transactions/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payout` | query | `string` | no | Only transactions included in this automatic Stripe payout. Leave blank to list all balance transactions. |
| `created` | query | `object` | no | Only return records created during this date interval. |
| `created[gt]` | query | `date` | no | After this date, exclusive. |
| `created[gte]` | query | `date` | no | On or after this date, inclusive. |
| `created[lt]` | query | `date` | no | Before this date, exclusive. |
| `created[lte]` | query | `date` | no | On or before this date, inclusive. |
