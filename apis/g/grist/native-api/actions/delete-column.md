# Delete Column with Grist

Deletes a column from a Grist table.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/docs/:docId/tables/:tableId/columns/:colId`
- **Base URL:** `https://docs.getgrist.com/api`
- **Official documentation:** [Delete Column](https://support.getgrist.com/api/#tag/columns/operation/deleteColumn)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID |
| `tableId` | path | `string` | yes | Table ID (e.g. Table1) |
| `colId` | path | `string` | yes | Column ID to delete |
