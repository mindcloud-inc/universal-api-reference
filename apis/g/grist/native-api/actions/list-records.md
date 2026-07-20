# List Records with Grist

Finds records in a Grist table.

## Endpoint

- **Method:** `GET`
- **Path:** `/docs/:docId/tables/:tableId/records`
- **Base URL:** `https://docs.getgrist.com/api`
- **Official documentation:** [List Records](https://support.getgrist.com/api/#tag/records/operation/listRecords)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID |
| `tableId` | path | `list<string>` | yes | Table ID (e.g. Table1) |
| `filter` | query | `string` | no | JSON filter object, e.g. {"Name": ["Alice"]} |
| `sort` | query | `string` | no | Comma-separated columns, prefix - for desc |
| `limit` | query | `number` | no | Max records to return |
| `hidden` | query | `boolean` | no | Include hidden columns |
