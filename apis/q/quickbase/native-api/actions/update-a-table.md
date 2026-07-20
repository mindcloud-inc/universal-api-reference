# Update a Table with Quickbase

Updates an existing table in Quickbase.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/tables/:tableId`
- **Base URL:** `https://api.quickbase.com`
- **Official documentation:** [Update a Table](https://developer.quickbase.com/operation/updateTable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | query | `string` | yes | The Quickbase app identifier. |
| `tableId` | path | `string` | yes | The Quickbase table identifier. |
| `name` | body | `string` | no | Optional new table name. |
| `description` | body | `string` | no | Optional new description for the table. |
| `singleRecordName` | body | `string` | no | Optional new singular label for records in the table. |
| `pluralRecordName` | body | `string` | no | Optional new plural label for records in the table. |
