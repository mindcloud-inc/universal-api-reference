# Create Project NFT with Underdog Protocol

Creates a new project NFT in Underdog Protocol.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/projects/:transferable/:projectId/nfts`
- **Base URL:** `https://dev.underdogprotocol.com`
- **Official documentation:** [Create Project NFT](https://docs.underdogprotocol.com/resources/projects/nfts/create-an-nft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transferable` | path | `list` | yes | Value must be either 't' for transferable or 'n' for non-transferable Accepted values: `n`, `t`. |
| `projectId` | path | `number` | yes | — |
| `name` | body | `string` | yes | Name stored as on-chain metadata |
| `symbol` | body | `string` | no | Symbol stored as on-chain metadata |
| `description` | body | `string` | no | Description stored in the metadata |
| `image` | body | `string` | yes | Image URL for your NFT |
| `animationUrl` | body | `string` | no | Animation URL for your NFT |
| `attributes` | body | `object` | no | Key-value pairs of your NFT attributes |
| `receiverAddress` | body | `string` | no | Wallet address that will receive the NFT |
| `upsert` | body | `boolean` | no | If true, will update the NFT if one with the same owner / claimer exists |
