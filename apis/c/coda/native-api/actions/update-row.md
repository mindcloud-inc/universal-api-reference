# Update Row with Coda

Updates a row in a Coda table.

## Endpoint

- **Method:** `PUT`
- **Path:** `/docs/:docId/tables/:tableIdOrName/rows/:rowIdOrName`
- **Base URL:** `https://coda.io/apis/v1`
- **Official documentation:** [Update Row](https://coda.io/developers/apis/v1#tag/Rows/operation/updateRow)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `docId` | path | `list` | yes |
| `tableIdOrName` | path | `list` | yes |
| `rowIdOrName` | path | `list` | yes |
| `disableParsing` | query | `boolean` | no |
| `row` | body | `object` | yes |
| `row.cells[]` | body | `array<object>` | yes |
| `row.cells[].column` | body | `list` | yes |
| `row.cells[].value` | body | `string` | yes |
