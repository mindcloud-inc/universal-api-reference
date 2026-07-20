# Get Latest Block with Chainstream

Retrieves the latest blockchain block from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/blockchain/:chain/latest_block`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Get Latest Block](https://docs.chainstream.io/en/api-reference/endpoint/data/blockchain/v2/blockchain-chain-latest_block-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | A chain name listed in supported networks. |
