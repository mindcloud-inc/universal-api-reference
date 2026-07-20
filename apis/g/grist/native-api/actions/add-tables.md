# Add Tables with Grist

Creates new tables in a Grist document.

## Endpoint

- **Method:** `POST`
- **Path:** `/docs/:docId/tables`
- **Base URL:** `https://docs.getgrist.com/api`
- **Official documentation:** [Add Tables](https://support.getgrist.com/api/#tag/tables/operation/addTables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID |
| `tables` | body | `string` | yes | Array of {id: 'TableName', columns: [{id: 'ColName', fields: {type: 'Text'}}]} |
