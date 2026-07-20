# List Customers with GoCardless

Finds customers in your GoCardless account.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [List Customers](https://developer.gocardless.com/api-reference/#customers-list-customers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action_required` | query | `boolean` | no | — |
| `created_at` | query | `object` | no | — |
| `created_at[gt]` | query | `date` | no | — |
| `created_at[gte]` | query | `date` | no | — |
| `created_at[lt]` | query | `date` | no | — |
| `created_at[lte]` | query | `date` | no | — |
| `currency` | query | `list` | no | Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `sort_field` | query | `list` | no | Accepted values: `0`, `1`, `2`. |
| `sort_direction` | query | `list` | no | Accepted values: `0`, `1`. |
