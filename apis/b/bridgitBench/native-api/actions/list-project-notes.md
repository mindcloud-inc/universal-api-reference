# List Project Notes with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/notes`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Project Notes](https://developers.gobridgit.com/reference/projectnotes_query)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID the note belongs to |
