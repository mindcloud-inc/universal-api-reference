# Get NFT Metadata with OpenSea

Retrieves NFT metadata from OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/metadata/{chain}/{contractAddress}/{tokenId}`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get NFT Metadata](https://docs.opensea.io/reference/get_nft_metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | The blockchain on which to filter the results |
| `contractAddress` | path | `string` | yes | The unique public blockchain identifier for the contract |
| `tokenId` | path | `string` | yes | The NFT token id |
