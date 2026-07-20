# Get Project with Underdog Protocol

Retrieves a project from Underdog Protocol.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:transferable/:projectId`
- **Base URL:** `https://dev.underdogprotocol.com`
- **Official documentation:** [Get Project](https://docs.underdogprotocol.com/resources/projects/methods/retrieve-a-project)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transferable` | path | `list` | yes | Value must be either 't' for transferable or 'n' for non-transferable Accepted values: `n`, `t`. |
| `projectId` | path | `number` | yes | — |
| `page` | query | `number` | no | — |
| `limit` | query | `number` | no | — |
| `sortBy` | query | `string` | no | — |
| `orderBy` | query | `list` | no | Accepted values: `asc`, `desc`. |
