# Get Row with Coda

Retrieves row details from a Coda table.

## Endpoint

- **Method:** `GET`
- **Path:** `/docs/:docId/tables/:tableIdOrName/rows/:rowIdOrName`
- **Base URL:** `https://coda.io/apis/v1`
- **Official documentation:** [Get Row](https://coda.io/developers/apis/v1#tag/Rows/operation/getRow)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `docId` | path | `list` | yes |
| `tableIdOrName` | path | `list` | yes |
| `rowIdOrName` | path | `list` | yes |
| `useColumnNames` | query | `boolean` | no |
| `valueFormat` | query | `string` | no |
