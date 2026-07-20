# Get Source Table Columns Config with Fivetran

Retrieves source table column configuration from Fivetran.

## Endpoint

- **Method:** `GET`
- **Path:** `/connections/[:connectionId]/schemas/[:schema]/tables/[:table]/columns`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Get Source Table Columns Config](https://fivetran.com/docs/rest-api/api-reference/connection-schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | The unique identifier for the connection within Fivetran. |
| `schema` | path | `string` | yes | The database schema name within the destination. |
| `table` | path | `string` | yes | The source table name from the connection schema. |
