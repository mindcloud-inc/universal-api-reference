# List Project NFTs with Underdog Protocol

Retrieves NFTs from a project in Underdog Protocol.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:transferable/:projectId/nfts`
- **Base URL:** `https://dev.underdogprotocol.com`
- **Official documentation:** [List Project NFTs](https://docs.underdogprotocol.com/resources/projects/nfts/list-all-nfts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transferable` | path | `list` | yes | Value must be either 't' for transferable or 'n' for non-transferable Accepted values: `n`, `t`. |
| `projectId` | path | `number` | yes | — |
| `page` | query | `number` | no | — |
| `limit` | query | `number` | no | — |
| `ownerAddress` | query | `string` | no | — |
