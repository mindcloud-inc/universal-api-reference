# Get Token Stats with Chainstream

Retrieves token stats from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/token/:chain/:tokenAddress/stats`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Get Token Stats](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-chain-tokenaddress-stats-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | Supported blockchain chain |
| `tokenAddress` | path | `string` | yes | Token contract address |
