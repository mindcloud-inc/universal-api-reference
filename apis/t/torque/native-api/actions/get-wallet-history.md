# Get Wallet History with Torque

## Endpoint

- **Method:** `GET`
- **Path:** `/moralis/wallet-history`
- **Base URL:** `https://app.torque.fi/api`
- **Official documentation:** [Get Wallet History](https://docs.torque.fi/business/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | query | `string` | yes | Wallet address to query. |
| `chain` | query | `string` | no | — |
| `limit` | query | `number` | no | Maximum number of records to return. |
