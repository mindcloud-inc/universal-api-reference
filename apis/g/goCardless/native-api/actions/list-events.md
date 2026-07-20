# List Events with GoCardless

Finds events in your GoCardless account.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [List Events](https://developer.gocardless.com/api-reference/#events-list-events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `action` | query | `string` | no |
| `billing_request` | query | `string` | no |
| `created_at` | query | `object` | no |
| `created_at[gt]` | query | `date` | no |
| `created_at[gte]` | query | `date` | no |
| `created_at[lt]` | query | `date` | no |
| `created_at[lte]` | query | `date` | no |
| `creditor` | query | `string` | no |
| `export` | query | `string` | no |
| `include` | query | `string` | no |
| `instalment_schedule` | query | `string` | no |
| `mandate` | query | `string` | no |
| `outbound_payment` | query | `string` | no |
| `parent_event` | query | `string` | no |
| `payer_authorisation` | query | `string` | no |
| `payment` | query | `string` | no |
| `payment_account_transaction` | query | `string` | no |
| `payout` | query | `string` | no |
| `refund` | query | `string` | no |
| `resource_type` | query | `string` | no |
| `scheme_identifier` | query | `string` | no |
| `subscription` | query | `string` | no |
