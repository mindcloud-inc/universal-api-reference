# Update Tables with Grist

Updates existing tables in a Grist document.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/docs/:docId/tables`
- **Base URL:** `https://docs.getgrist.com/api`
- **Official documentation:** [Update Tables](https://support.getgrist.com/api/#tag/tables/operation/modifyTables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID |
| `tables` | body | `string` | yes | JSON array of table patch objects, e.g. [{"id":"CurrentTableId","fields":{"tableId":"NewTableId"}}] |
