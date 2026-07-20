# Edit NFT with Crossmint

Updates NFT metadata in Crossmint.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/2022-06-09/collections/:collectionId/nfts/:id`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Edit NFT](https://docs.crossmint.com/api-reference/minting/nfts/edit-nft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Collection identifier. |
| `id` | path | `string` | yes | NFT identifier returned by Crossmint. |
| `metadata` | body | `object` | yes | Updated NFT metadata object. |
| `reuploadLinkedFiles` | body | `boolean` | no | Whether metadata URLs should be resolved and reuploaded to IPFS. Defaults to true. |
