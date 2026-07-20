# Re-sync Connection with Fivetran

Starts a re-sync for a connection in Fivetran.

## Endpoint

- **Method:** `POST`
- **Path:** `/connections/[:connectionId]/resync`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Re-sync Connection](https://fivetran.com/docs/rest-api/api-reference/connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | The unique identifier for the connection within Fivetran. |
| `scope` | body | `object` | no | Optional map of schemas and tables to re-sync. |
