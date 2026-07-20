# Get NFTs By Contract with OpenSea

Retrieves NFTs for a contract in OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/chain/{chain}/contract/{address}/nfts`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get NFTs By Contract](https://docs.opensea.io/reference/get_nfts_by_contract)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | path | `string` | yes | Contract address |
| `chain` | path | `string` | yes | The blockchain on which to filter the results |
| `limit` | query | `number` | no | Number of items to return per page |
| `next.value` | query | `string` | no | — |
