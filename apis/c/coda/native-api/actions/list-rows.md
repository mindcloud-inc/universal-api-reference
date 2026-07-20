# List Rows with Coda

Retrieves rows from a Coda table.

## Endpoint

- **Method:** `GET`
- **Path:** `/docs/:docId/tables/:tableIdOrName/rows`
- **Base URL:** `https://coda.io/apis/v1`
- **Official documentation:** [List Rows](https://coda.io/developers/apis/v1#tag/Rows/operation/listRows)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `docId` | path | `list` | yes |
| `tableIdOrName` | path | `list` | yes |
| `query` | query | `string` | no |
| `useColumnNames` | query | `boolean` | no |
| `valueFormat` | query | `string` | no |
| `visibleOnly` | query | `boolean` | no |
| `syncToken` | query | `string` | no |
