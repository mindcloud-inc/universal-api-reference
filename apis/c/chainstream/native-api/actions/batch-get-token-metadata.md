# Batch Get Token Metadata with Chainstream

Retrieves token metadata in bulk from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/token/:chain/metadata/multi`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Batch Get Token Metadata](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-chain-metadata-multi-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | Supported blockchain chain |
| `tokenAddresses` | query | `string` | yes | Comma-separated list of token addresses |
