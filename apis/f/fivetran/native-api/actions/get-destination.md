# Get Destination with Fivetran

Retrieves a destination from your Fivetran account.

## Endpoint

- **Method:** `GET`
- **Path:** `/destinations/[:destinationId]`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Get Destination](https://fivetran.com/docs/rest-api/api-reference/destination)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destinationId` | path | `string` | yes | The unique identifier for the destination within Fivetran. |
