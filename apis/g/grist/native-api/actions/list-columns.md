# List Columns with Grist

Finds columns in a Grist table.

## Endpoint

- **Method:** `GET`
- **Path:** `/docs/:docId/tables/:tableId/columns`
- **Base URL:** `https://docs.getgrist.com/api`
- **Official documentation:** [List Columns](https://support.getgrist.com/api/#tag/columns/operation/listColumns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID |
| `tableId` | path | `list<string>` | yes | Table ID (e.g. Table1) |
| `hidden` | query | `boolean` | no | Include hidden columns |
