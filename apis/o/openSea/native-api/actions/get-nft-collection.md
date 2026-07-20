# Get Collection By NFT with OpenSea

Retrieves an NFT's collection from OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/chain/{chain}/contract/{address}/nfts/{identifier}/collection`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Collection By NFT](https://docs.opensea.io/reference/get_nft_collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | The blockchain on which to filter the results |
| `address` | path | `string` | yes | The unique public blockchain identifier for the contract |
| `identifier` | path | `string` | yes | The NFT token id |
