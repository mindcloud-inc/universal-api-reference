# Get Connection with Fivetran

Retrieves a connection from your Fivetran account.

## Endpoint

- **Method:** `GET`
- **Path:** `/connections/[:connectionId]`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Get Connection](https://fivetran.com/docs/rest-api/api-reference/connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | The unique identifier for the connection within Fivetran. |
