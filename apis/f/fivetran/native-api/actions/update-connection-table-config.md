# Update Connection Table Config with Fivetran

Updates table configuration for a connection schema in Fivetran.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/connections/[:connectionId]/schemas/[:schemaName]/tables/[:tableName]`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Update Connection Table Config](https://fivetran.com/docs/rest-api/api-reference/connection-schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columns` | body | `object` | no | Column configuration object for the table. |
| `connectionId` | path | `string` | yes | The unique identifier for the connection within Fivetran. |
| `enabled` | body | `boolean` | yes | Whether syncing the table into the destination is enabled. |
| `schemaName` | path | `string` | yes | The schema name as stored in the connection schema config. |
| `tableName` | path | `string` | yes | The table name as stored in the connection schema config. |
