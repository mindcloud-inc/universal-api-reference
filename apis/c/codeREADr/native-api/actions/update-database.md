# Update Database with CodeREADr

Updates an existing validation database in CodeREADr.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/`
- **Base URL:** `https://api.codereadr.com`
- **Official documentation:** [Update Database](https://secure.codereadr.com/apidocs/Databases.md#update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `database_id` | body | `string` | yes | Database to rename. |
| `database_name` | body | `string` | yes | New name for the database. |
