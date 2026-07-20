# Revoke Project NFT with Underdog Protocol

Revokes a project NFT in Underdog Protocol.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/projects/n/:projectId/nfts/:nftId/revoke`
- **Base URL:** `https://dev.underdogprotocol.com`
- **Official documentation:** [Revoke Project NFT](https://docs.underdogprotocol.com/resources/projects/nfts/revoke-an-nft)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `nftId` | path | `number` | yes |
