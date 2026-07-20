# Replace Records with Grist

Replaces records in a Grist table.

## Endpoint

- **Method:** `PUT`
- **Path:** `/docs/:docId/tables/:tableId/records`
- **Base URL:** `https://docs.getgrist.com/api`
- **Official documentation:** [Replace Records](https://support.getgrist.com/api/#tag/records/operation/replaceRecords)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID |
| `tableId` | path | `list<string>` | yes | Table ID (e.g. Table1) |
| `records` | body | `string` | yes | Array of {require: {col: val}, fields: {col: val}} |
| `noparse` | query | `boolean` | no | Skip string parsing |
| `onmany` | query | `string` | no | When multiple match: first, none, or all |
| `noadd` | query | `boolean` | no | Do not add new records |
| `noupdate` | query | `boolean` | no | Do not update existing records |
