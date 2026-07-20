# Get Connection State with Fivetran

Retrieves sync state for a connection in Fivetran.

## Endpoint

- **Method:** `GET`
- **Path:** `/connections/[:connectionId]/state`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Get Connection State](https://fivetran.com/docs/rest-api/api-reference/connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | The unique identifier for the connection within Fivetran. |
