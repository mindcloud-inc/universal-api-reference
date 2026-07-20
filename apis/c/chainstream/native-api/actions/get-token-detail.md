# Get Token Detail with Chainstream

Retrieves token details from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/token/:chain/:tokenAddress`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Get Token Detail](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-chain-tokenaddress-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | Supported blockchain chain |
| `tokenAddress` | path | `string` | yes | Token address |
