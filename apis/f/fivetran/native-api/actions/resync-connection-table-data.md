# Re-sync Connection Table Data with Fivetran

Re-syncs table data for a connection in Fivetran.

## Endpoint

- **Method:** `POST`
- **Path:** `/connections/[:connectionId]/schemas/tables/resync`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Re-sync Connection Table Data](https://fivetran.com/docs/rest-api/api-reference/connection-schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | The unique identifier for the connection within Fivetran. |
| `schema` | body | `list<string>` | no | Schema names to re-sync, sent as the documented schema array in the JSON request body. |
