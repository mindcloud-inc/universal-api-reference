# List Customer Bank Accounts with GoCardless

Finds customer bank accounts in GoCardless.

## Endpoint

- **Method:** `GET`
- **Path:** `/customer_bank_accounts`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [List Customer Bank Accounts](https://developer.gocardless.com/api-reference/#customer-bank-accounts-list-customer-bank-accounts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer` | query | `string` | no |
| `enabled` | query | `boolean` | no |
| `created_at` | query | `object` | no |
| `created_at[gt]` | query | `date` | no |
| `created_at[gte]` | query | `date` | no |
| `created_at[lt]` | query | `date` | no |
| `created_at[lte]` | query | `date` | no |
