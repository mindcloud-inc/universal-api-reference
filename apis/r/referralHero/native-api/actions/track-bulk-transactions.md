# Track Bulk Transactions with ReferralHero

Creates bulk subscriber transactions in ReferralHero.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:uuid/subscribers/add_bulk_transactions`
- **Base URL:** `https://app.referralhero.com/api/v2`
- **Official documentation:** [Track Bulk Transactions](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#track-transactions-single-transaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactions[]` | body | `array<object>` | yes | JSON array of transactions to process in bulk. |
| `uuid` | path | `string` | yes | ReferralHero list UUID. |
