# Burn NFT with Crossmint

Burns an NFT from Crossmint.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/2022-06-09/collections/:collectionId/nfts/:id`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Burn NFT](https://docs.crossmint.com/api-reference/minting/nfts/burn-nft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Collection identifier. |
| `id` | path | `string` | yes | NFT identifier returned by Crossmint. |
