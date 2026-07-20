# List Directories with Linkbreakers

Retrieves a list of directories from Linkbreakers.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/directories`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [List Directories](https://linkbreakers.com/help/api/directories)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parentDirectoryId` | query | `string` | no | Filter directories by parent directory ID. |
| `search` | query | `string` | no | Search query to filter directories by name. |
| `includeRoot` | query | `boolean` | no | Also include root-level directories when filtering by parent. |
| `recursive` | query | `boolean` | no | Return directories recursively. |
