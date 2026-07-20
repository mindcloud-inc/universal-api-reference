# Get Table with Coda

Retrieves table details from a Coda doc.

## Endpoint

- **Method:** `GET`
- **Path:** `/docs/:docId/tables/:tableIdOrName`
- **Base URL:** `https://coda.io/apis/v1`
- **Official documentation:** [Get Table](https://coda.io/developers/apis/v1#tag/Tables/operation/getTable)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `docId` | path | `list` | yes |
| `tableIdOrName` | path | `list` | yes |
| `useUpdatedTableLayouts` | query | `boolean` | no |
