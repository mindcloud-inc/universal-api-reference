# List Subscriptions with GoCardless

Finds subscriptions in your GoCardless account.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscriptions`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [List Subscriptions](https://developer.gocardless.com/api-reference/#subscriptions-list-subscriptions)

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
| `customer` | query | `string` | no |
| `mandate` | query | `string` | no |
| `status` | query | `string` | no |
