# Get Token Creation with Chainstream

Retrieves token creation details from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/token/:chain/:tokenAddress/creation`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Get Token Creation](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-chain-tokenaddress-creation-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | Supported blockchain chain |
| `tokenAddress` | path | `string` | yes | Token contract address |
