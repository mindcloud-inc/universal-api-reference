# List Columns with Coda

Retrieves columns from a Coda table.

## Endpoint

- **Method:** `GET`
- **Path:** `/docs/:docId/tables/:tableIdOrName/columns`
- **Base URL:** `https://coda.io/apis/v1`
- **Official documentation:** [List Columns](https://coda.io/developers/apis/v1#tag/Columns/operation/listColumns)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `docId` | path | `list` | yes |
| `tableIdOrName` | path | `list` | yes |
| `visibleOnly` | query | `boolean` | no |
