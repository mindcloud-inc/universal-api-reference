# Get Top Gaining Tokens with Torque

## Endpoint

- **Method:** `GET`
- **Path:** `/moralis/token-top-gainers`
- **Base URL:** `https://app.torque.fi/api`
- **Official documentation:** [Get Top Gaining Tokens](https://docs.torque.fi/business/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | query | `string` | yes | Wallet address. Torque's live endpoint currently requires address for this route. |
| `chain` | query | `string` | no | — |
| `limit` | query | `number` | no | Maximum number of records to return. |
