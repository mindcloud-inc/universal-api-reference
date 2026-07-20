# List Interactions By Connection with Conveyor

Retrieves interactions for a connection from Conveyor.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/interactions/connections/:connection_id`
- **Base URL:** `https://api.conveyor.com/api`
- **Official documentation:** [List Interactions By Connection](https://docs.conveyor.com/reference/get-interactions-by-connection-id)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connection_id` | path | `string` | yes | Connection identifier. |
| `type` | query | `string` | no | Interaction type filter. |
| `created_at_start` | query | `date` | no | Start of created-at date range. |
| `created_at_end` | query | `date` | no | End of created-at date range. |
