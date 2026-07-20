# List Wallet Transactions with Monta

Retrieves wallet transactions from Monta.

## Endpoint

- **Method:** `GET`
- **Path:** `/wallet-transactions`
- **Base URL:** `https://public-api.monta.com/api/v1`
- **Official documentation:** [List Wallet Transactions](https://docs.public-api.monta.com/reference/get-wallet-transactions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `state` | query | `list<string>` | no | Only return wallet transactions in this state. Accepted values: `complete`, `failed`, `pending`, `reserved`. |
| `fromDate` | query | `date` | no | Only return wallet transactions created at or after this ISO 8601 date-time. |
| `toDate` | query | `date` | no | Only return wallet transactions created at or before this ISO 8601 date-time. |
