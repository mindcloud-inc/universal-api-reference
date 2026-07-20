# List Tables with Coda

Retrieves tables from a Coda doc.

## Endpoint

- **Method:** `GET`
- **Path:** `/docs/:docId/tables`
- **Base URL:** `https://coda.io/apis/v1`
- **Official documentation:** [List Tables](https://coda.io/developers/apis/v1#tag/Tables/operation/listTables)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `docId` | path | `list` | yes |
| `tableTypes[]` | query | `array<string>` | no |
