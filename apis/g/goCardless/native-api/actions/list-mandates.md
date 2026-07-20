# List Mandates with GoCardless

Finds mandates in your GoCardless account.

## Endpoint

- **Method:** `GET`
- **Path:** `/mandates`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [List Mandates](https://developer.gocardless.com/api-reference/#mandates-list-mandates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_at` | query | `object` | no | Created-at range filters for mandate records. |
| `created_at[gt]` | query | `date` | no | — |
| `created_at[gte]` | query | `date` | no | — |
| `created_at[lt]` | query | `date` | no | — |
| `created_at[lte]` | query | `date` | no | — |
| `creditor` | query | `string` | no | — |
| `customer` | query | `string` | no | — |
| `customer_bank_account` | query | `string` | no | — |
| `mandate_type` | query | `string` | no | — |
| `reference` | query | `string` | no | — |
| `scheme` | query | `string` | no | — |
| `status` | query | `string` | no | — |
