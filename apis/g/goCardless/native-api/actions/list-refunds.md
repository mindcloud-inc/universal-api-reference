# List Refunds with GoCardless

Finds refunds in your GoCardless account.

## Endpoint

- **Method:** `GET`
- **Path:** `/refunds`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [List Refunds](https://developer.gocardless.com/api-reference/#refunds-list-refunds)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `created_at` | query | `object` | no |
| `created_at[gt]` | query | `date` | no |
| `created_at[gte]` | query | `date` | no |
| `created_at[lt]` | query | `date` | no |
| `created_at[lte]` | query | `date` | no |
| `mandate` | query | `string` | no |
| `payment` | query | `string` | no |
| `refund_type` | query | `string` | no |
