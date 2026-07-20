# Update Connection Schema Config with Fivetran

Updates schema configuration for a connection in Fivetran.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/connections/[:connectionId]/schemas`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Update Connection Schema Config](https://fivetran.com/docs/rest-api/api-reference/connection-schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | The unique identifier for the connection within Fivetran. |
| `schema_change_handling` | body | `string` | no | How Fivetran should handle new schemas, tables, and columns. |
| `schemas` | body | `object` | no | The set of schemas within the connection schema config. |
