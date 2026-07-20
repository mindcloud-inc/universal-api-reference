# Get Token Security with Chainstream

Retrieves token security details from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/token/:chain/:tokenAddress/security`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Get Token Security](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-chain-tokenaddress-security-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | Supported blockchain chain |
| `tokenAddress` | path | `string` | yes | Token contract address |
