# Add Records with Grist

Creates new records in a Grist table.

## Endpoint

- **Method:** `POST`
- **Path:** `/docs/:docId/tables/:tableId/records`
- **Base URL:** `https://docs.getgrist.com/api`
- **Official documentation:** [Add Records](https://support.getgrist.com/api/#tag/records/operation/addRecords)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID |
| `tableId` | path | `list<string>` | yes | Table ID (e.g. Table1) |
| `records` | body | `list<string>` | yes | Array of {fields: {col: val}} |
| `noparse` | query | `boolean` | no | Skip string parsing |
