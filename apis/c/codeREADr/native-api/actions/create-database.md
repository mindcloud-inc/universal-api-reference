# Create Database with CodeREADr

Creates a new validation database in CodeREADr.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/`
- **Base URL:** `https://api.codereadr.com`
- **Official documentation:** [Create Database](https://secure.codereadr.com/apidocs/Databases.md#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `database_name` | body | `string` | yes | Name for the new database. |
| `case_sensitivity` | body | `string` | no | Set to 1 for case-sensitive values or 0 for case-insensitive values. |
