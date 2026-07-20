# Delete Row with Coda

Deletes a row from a Coda table.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/docs/:docId/tables/:tableIdOrName/rows/:rowIdOrName`
- **Base URL:** `https://coda.io/apis/v1`
- **Official documentation:** [Delete Row](https://coda.io/developers/apis/v1#tag/Rows/operation/deleteRow)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `docId` | path | `list` | yes |
| `tableIdOrName` | path | `list` | yes |
| `rowIdOrName` | path | `list` | yes |
