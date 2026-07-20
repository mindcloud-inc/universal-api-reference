# Get NFT with Crossmint

Retrieves NFT status from Crossmint.

## Endpoint

- **Method:** `GET`
- **Path:** `/2022-06-09/collections/:collectionId/nfts/:id`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Get NFT](https://docs.crossmint.com/api-reference/minting/nfts/mint-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Collection identifier. |
| `id` | path | `string` | yes | NFT identifier returned by Crossmint. |
