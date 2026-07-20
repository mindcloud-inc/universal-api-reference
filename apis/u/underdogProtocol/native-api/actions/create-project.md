# Create Project with Underdog Protocol

Creates a new project in Underdog Protocol.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/projects`
- **Base URL:** `https://dev.underdogprotocol.com`
- **Official documentation:** [Create Project](https://docs.underdogprotocol.com/resources/projects/methods/create-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name stored as on-chain metadata |
| `symbol` | body | `string` | no | Symbol stored as on-chain metadata |
| `description` | body | `string` | no | Description stored in the metadata |
| `image` | body | `string` | yes | Image URL for your NFT |
| `transferable` | body | `boolean` | yes | Whether or not the NFTs in this project can be transferred |
| `animationUrl` | body | `string` | no | Animation URL for your NFT |
