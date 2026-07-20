# Create a Table with Quickbase

Creates a new table in Quickbase.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/tables`
- **Base URL:** `https://api.quickbase.com`
- **Official documentation:** [Create a Table](https://developer.quickbase.com/operation/createTable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | query | `string` | yes | The Quickbase app identifier. |
| `name` | body | `string` | yes | The table name. |
| `description` | body | `string` | no | Optional description for the table. |
| `singleRecordName` | body | `string` | no | Optional singular label for records in the table. |
| `pluralRecordName` | body | `string` | no | Optional plural label for records in the table. |
