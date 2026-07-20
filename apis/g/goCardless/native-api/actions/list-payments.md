# List Payments with GoCardless

Finds payments in your GoCardless account.

## Endpoint

- **Method:** `GET`
- **Path:** `/payments`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [List Payments](https://developer.gocardless.com/api-reference/#payments-list-payments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_at` | query | `object` | no | Filter payments by creation time. |
| `created_at[gt]` | query | `date` | no | Limit to records created after the specified date-time. |
| `created_at[gte]` | query | `date` | no | Limit to records created on or after the specified date-time. |
| `created_at[lt]` | query | `date` | no | Limit to records created before the specified date-time. |
| `created_at[lte]` | query | `date` | no | Limit to records created on or before the specified date-time. |
| `creditor` | query | `string` | no | Filter payments to a specific creditor. |
| `customer` | query | `string` | no | Filter payments to a specific customer. |
| `mandate` | query | `string` | no | Filter payments to a specific mandate. |
| `status` | query | `string` | no | Filter payments by status. |
| `subscription` | query | `string` | no | Filter payments to a specific subscription. |
| `sort_direction` | query | `string` | no | Control the sort direction for the returned payments. |
