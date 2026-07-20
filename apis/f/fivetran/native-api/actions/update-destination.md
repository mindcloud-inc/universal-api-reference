# Update Destination with Fivetran

Updates an existing destination in your Fivetran account.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/destinations/[:destinationId]`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Update Destination](https://fivetran.com/docs/rest-api/api-reference/destination)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `config` | body | `object` | no | Destination setup configuration object. |
| `destinationId` | path | `string` | yes | The unique identifier for the destination within Fivetran. |
| `time_zone_offset` | body | `string` | yes | The time zone offset used for the Fivetran sync schedule. |
