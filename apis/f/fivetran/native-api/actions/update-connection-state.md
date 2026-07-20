# Update Connection State with Fivetran

Updates sync state for a connection in Fivetran.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/connections/[:connectionId]/state`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Update Connection State](https://fivetran.com/docs/rest-api/api-reference/connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | The unique identifier for the connection within Fivetran. |
