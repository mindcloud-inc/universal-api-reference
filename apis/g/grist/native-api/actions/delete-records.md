# Delete Records with Grist

Deletes records from a Grist table.

## Endpoint

- **Method:** `POST`
- **Path:** `/docs/:docId/tables/:tableId/records/delete`
- **Base URL:** `https://docs.getgrist.com/api`
- **Official documentation:** [Delete Records](https://support.getgrist.com/api/#tag/records/operation/deleteRecords)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID |
| `tableId` | path | `string` | yes | Table ID (e.g. Table1) |
| `records[]` | body | `array<number>` | yes | Array of integer record IDs to delete, e.g. [1,2,3] |
