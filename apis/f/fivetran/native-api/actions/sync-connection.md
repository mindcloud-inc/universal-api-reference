# Sync Connection with Fivetran

Starts a sync for a connection in Fivetran.

## Endpoint

- **Method:** `POST`
- **Path:** `/connections/[:connectionId]/sync`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Sync Connection](https://fivetran.com/docs/rest-api/api-reference/connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | The unique identifier for the connection within Fivetran. |
| `force` | body | `boolean` | no | Stop and re-run the sync if the connection is currently syncing. |
