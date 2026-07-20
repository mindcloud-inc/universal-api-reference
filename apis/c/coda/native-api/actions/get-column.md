# Get Column with Coda

Retrieves column details from a Coda table.

## Endpoint

- **Method:** `GET`
- **Path:** `/docs/:docId/tables/:tableIdOrName/columns/:columnIdOrName`
- **Base URL:** `https://coda.io/apis/v1`
- **Official documentation:** [Get Column](https://coda.io/developers/apis/v1#tag/Columns/operation/getColumn)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `docId` | path | `list` | yes |
| `tableIdOrName` | path | `list` | yes |
| `columnIdOrName` | path | `list` | yes |
