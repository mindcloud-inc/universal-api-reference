# Delete Database Value with CodeREADr

Deletes a database value from CodeREADr.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/`
- **Base URL:** `https://api.codereadr.com`
- **Official documentation:** [Delete Database Value](https://secure.codereadr.com/apidocs/Databases.md#deletevalue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `database_id` | body | `string` | yes | Database to delete the value from. |
| `value` | body | `string` | yes | Barcode value to delete. |
