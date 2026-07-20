# Get Token Holders with Chainstream

Retrieves token holders from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/token/:chain/:tokenAddress/holders`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Get Token Holders](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-chain-tokenaddress-holders-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | Supported blockchain chain |
| `tokenAddress` | path | `string` | yes | Token contract address |
| `cursor` | query | `string` | no | Pagination cursor |
| `limit` | query | `string` | no | Number of results per page |
| `direction` | query | `string` | no | Pagination direction |
