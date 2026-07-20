# Update Records with Grist

Updates existing records in a Grist table.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/docs/:docId/tables/:tableId/records`
- **Base URL:** `https://docs.getgrist.com/api`
- **Official documentation:** [Update Records](https://support.getgrist.com/api/#tag/records/operation/modifyRecords)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID |
| `tableId` | path | `string` | yes | Table ID (e.g. Table1) |
| `records` | body | `string` | yes | Array of {id: rowId, fields: {col: val}} |
| `noparse` | query | `boolean` | no | Skip string parsing |
