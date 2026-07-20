# Get Project Stats with Underdog Protocol

Retrieves project stats from Underdog Protocol.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:transferable/:projectId/stats`
- **Base URL:** `https://dev.underdogprotocol.com`
- **Official documentation:** [Get Project Stats](https://docs.underdogprotocol.com/resources/projects/methods/retrieve-project-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transferable` | path | `list` | yes | Value must be either 't' for transferable or 'n' for non-transferable Accepted values: `n`, `t`. |
| `projectId` | path | `number` | yes | — |
