# Reload Connection Schema Config with Fivetran

Reloads schema configuration for a connection in Fivetran.

## Endpoint

- **Method:** `POST`
- **Path:** `/connections/[:connectionId]/schemas/reload`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Reload Connection Schema Config](https://fivetran.com/docs/rest-api/api-reference/connection-schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | The unique identifier for the connection within Fivetran. |
| `exclude_mode` | body | `string` | no | Whether all schemas and tables are enabled or disabled during schema reload. |
