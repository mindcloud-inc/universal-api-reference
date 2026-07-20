# Update Database with Firebolt

Updates an existing database in Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineHost`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Update Database](https://docs.firebolt.io/reference-sql/commands/data-definition/alter-database)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineHost` | path | `string` | yes | System engine host to execute the ALTER DATABASE statement against. |
| `databaseName` | body | `string` | yes | The Firebolt database to alter. |
| `alterClause` | body | `string` | yes | The ALTER DATABASE clause, for example SET DESCRIPTION = 'Updated description' or RENAME TO new_database_name. |
