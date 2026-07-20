# Search Project NFTs with Underdog Protocol

Finds project NFTs in Underdog Protocol by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:transferable/:projectId/nfts/search`
- **Base URL:** `https://dev.underdogprotocol.com`
- **Official documentation:** [Search Project NFTs](https://docs.underdogprotocol.com/resources/projects/nfts/search-nfts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transferable` | path | `list` | yes | Value must be either 't' for transferable or 'n' for non-transferable Accepted values: `n`, `t`. |
| `projectId` | path | `number` | yes | — |
| `page` | query | `number` | no | — |
| `limit` | query | `number` | no | — |
| `search` | query | `string` | no | — |
