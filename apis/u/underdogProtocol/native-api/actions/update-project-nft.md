# Update Project NFT with Underdog Protocol

Updates an existing project NFT in Underdog Protocol.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/projects/:transferable/:projectId/nfts/:nftId`
- **Base URL:** `https://dev.underdogprotocol.com`
- **Official documentation:** [Update Project NFT](https://docs.underdogprotocol.com/resources/projects/nfts/update-an-nft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transferable` | path | `list` | yes | Value must be either 't' for transferable or 'n' for non-transferable Accepted values: `n`, `t`. |
| `projectId` | path | `number` | yes | — |
| `nftId` | path | `number` | yes | — |
| `description` | body | `string` | no | Description stored in the metadata |
| `image` | body | `string` | yes | Image URL for your NFT |
| `attributes` | body | `object` | no | Key-value pairs of your NFT attributes |
| `animationUrl` | body | `string` | no | Animation URL for your NFT |
