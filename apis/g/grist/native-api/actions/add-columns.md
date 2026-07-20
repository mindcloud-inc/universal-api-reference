# Add Columns with Grist

Creates new columns in a Grist table.

## Endpoint

- **Method:** `POST`
- **Path:** `/docs/:docId/tables/:tableId/columns`
- **Base URL:** `https://docs.getgrist.com/api`
- **Official documentation:** [Add Columns](https://support.getgrist.com/api/#tag/columns/operation/addColumns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID |
| `tableId` | path | `list<string>` | yes | Table ID (e.g. Table1) |
| `columns` | body | `string` | yes | Array of {id: 'ColName', fields: {type: 'Text', label: 'Column Label'}} |
