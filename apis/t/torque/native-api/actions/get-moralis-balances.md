# Get Moralis Balances with Torque

## Endpoint

- **Method:** `GET`
- **Path:** `/moralis/balances`
- **Base URL:** `https://app.torque.fi/api`
- **Official documentation:** [Get Moralis Balances](https://docs.torque.fi/business/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | query | `string` | yes | Wallet address to query. |
| `chain` | query | `string` | no | — |
| `limit` | query | `number` | no | Maximum number of records to return. |
| `exclude_spam` | query | `boolean` | no | — |
| `exclude_unverified_contracts` | query | `boolean` | no | — |
