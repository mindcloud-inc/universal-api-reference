# Push Button with Coda

Pushes a button in a Coda table row.

## Endpoint

- **Method:** `POST`
- **Path:** `/docs/:docId/tables/:tableIdOrName/rows/:rowIdOrName/buttons/:columnIdOrName`
- **Base URL:** `https://coda.io/apis/v1`
- **Official documentation:** [Push Button](https://coda.io/developers/apis/v1#tag/Rows/operation/pushButton)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `docId` | path | `list` | yes |
| `tableIdOrName` | path | `list` | yes |
| `rowIdOrName` | path | `list` | yes |
| `columnIdOrName` | path | `list` | yes |
