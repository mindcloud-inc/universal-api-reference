# Get Project NFT with Underdog Protocol

Retrieves a project NFT from Underdog Protocol.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:transferable/:projectId/nfts/:nftId`
- **Base URL:** `https://dev.underdogprotocol.com`
- **Official documentation:** [Get Project NFT](https://docs.underdogprotocol.com/resources/projects/nfts/retrieve-an-nft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transferable` | path | `list` | yes | Value must be either 't' for transferable or 'n' for non-transferable Accepted values: `n`, `t`. |
| `projectId` | path | `number` | yes | — |
| `nftId` | path | `number` | yes | — |
