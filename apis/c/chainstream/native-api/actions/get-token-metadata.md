# Get Token Metadata with Chainstream

Retrieves token metadata from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/token/:chain/:tokenAddress/metadata`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Get Token Metadata](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-chain-tokenaddress-metadata-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | Supported blockchain chain |
| `tokenAddress` | path | `string` | yes | Token contract address |
