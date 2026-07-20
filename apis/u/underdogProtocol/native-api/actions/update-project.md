# Update Project with Underdog Protocol

Updates an existing project in Underdog Protocol.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/projects/:transferable/:projectId`
- **Base URL:** `https://dev.underdogprotocol.com`
- **Official documentation:** [Update Project](https://docs.underdogprotocol.com/resources/projects/methods/update-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transferable` | path | `list` | yes | Value must be either 't' for transferable or 'n' for non-transferable Accepted values: `n`, `t`. |
| `projectId` | path | `number` | yes | — |
| `description` | body | `string` | no | Description stored in the metadata |
| `image` | body | `string` | yes | Image URL for your NFT |
| `animationUrl` | body | `string` | no | Animation URL for your NFT |
