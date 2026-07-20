# Upsert Rows with Coda

Inserts or updates rows in a Coda table.

## Endpoint

- **Method:** `POST`
- **Path:** `/docs/:docId/tables/:tableIdOrName/rows`
- **Base URL:** `https://coda.io/apis/v1`
- **Official documentation:** [Upsert Rows](https://coda.io/developers/apis/v1#tag/Rows/operation/upsertRows)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `docId` | path | `list` | yes |
| `tableIdOrName` | path | `list` | yes |
| `disableParsing` | query | `boolean` | no |
| `rows[]` | body | `array<object>` | yes |
| `keyColumns[]` | body | `array<string>` | no |
| `rows[].cells[]` | body | `array<object>` | yes |
| `rows[].cells[].column` | body | `list` | yes |
| `rows[].cells[].value` | body | `string` | yes |
