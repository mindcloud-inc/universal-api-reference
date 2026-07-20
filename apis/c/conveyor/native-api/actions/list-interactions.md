# List Interactions with Conveyor

Retrieves interactions for a program from Conveyor.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/interactions`
- **Base URL:** `https://api.conveyor.com/api`
- **Official documentation:** [List Interactions](https://docs.conveyor.com/reference/get-interactions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Interaction type filter. |
| `created_at_start` | query | `date` | no | Start of created-at date range. |
| `created_at_end` | query | `date` | no | End of created-at date range. |
