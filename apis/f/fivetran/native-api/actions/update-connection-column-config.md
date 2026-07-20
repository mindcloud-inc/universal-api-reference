# Update Connection Column Config with Fivetran

Updates column configuration for a connection schema in Fivetran.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/connections/[:connectionId]/schemas/[:schemaName]/tables/[:tableName]/columns/[:columnName]`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Update Connection Column Config](https://fivetran.com/docs/rest-api/api-reference/connection-schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columnName` | path | `string` | yes | The column name as stored in the connection schema config. |
| `connectionId` | path | `string` | yes | The unique identifier for the connection within Fivetran. |
| `enabled` | body | `boolean` | yes | Whether syncing the column into the destination is enabled. |
| `hashed` | body | `boolean` | no | Whether the column should be hashed. |
| `is_primary_key` | body | `boolean` | no | Whether the column is a primary key. |
| `schemaName` | path | `string` | yes | The schema name as stored in the connection schema config. |
| `tableName` | path | `string` | yes | The table name as stored in the connection schema config. |
