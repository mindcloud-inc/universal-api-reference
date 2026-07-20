# Mint NFT with Crossmint

Mints an NFT in Crossmint.

## Endpoint

- **Method:** `POST`
- **Path:** `/2022-06-09/collections/:collectionId/nfts`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Mint NFT](https://docs.crossmint.com/api-reference/minting/nfts/mint-nft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Collection identifier. |
| `metadata.name` | body | `string` | yes | NFT name. |
| `metadata.image` | body | `string` | yes | NFT image URL. |
| `metadata.description` | body | `string` | yes | NFT description. |
| `recipient` | body | `string` | yes | Recipient locator for the minted NFT. |
