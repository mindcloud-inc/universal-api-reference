# Replace Columns with Grist

Replaces columns in a Grist table.

## Endpoint

- **Method:** `PUT`
- **Path:** `/docs/:docId/tables/:tableId/columns`
- **Base URL:** `https://docs.getgrist.com/api`
- **Official documentation:** [Replace Columns](https://support.getgrist.com/api/#tag/columns/operation/replaceColumns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID |
| `tableId` | path | `list<string>` | yes | Table ID (e.g. Table1) |
| `columns` | body | `string` | yes | Array of column objects to add or update |
