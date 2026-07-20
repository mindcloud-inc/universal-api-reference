# List NFTs with Crossmint

Retrieves NFTs from a Crossmint collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/2022-06-09/collections/:collectionId/nfts`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [List NFTs](https://docs.crossmint.com/api-reference/minting/nfts/get-nfts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Collection identifier. For credential-template-backed tests, use the template ID returned by Crossmint. |
| `page` | query | `number` | yes | Page number starting at 1. |
| `perPage` | query | `number` | no | How many items to return in the page. |
