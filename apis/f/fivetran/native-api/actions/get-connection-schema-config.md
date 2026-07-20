# Get Connection Schema Config with Fivetran

Retrieves schema configuration for a connection in Fivetran.

## Endpoint

- **Method:** `GET`
- **Path:** `/connections/[:connectionId]/schemas`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Get Connection Schema Config](https://fivetran.com/docs/rest-api/api-reference/connection-schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | The unique identifier for the connection within Fivetran. |
