# List Assigned Conversations with Front

Retrieves conversations assigned to a teammate in Front.

## Endpoint

- **Method:** `GET`
- **Path:** `/teammates/:teammate_id/conversations`
- **Base URL:** `https://api2.frontapp.com`
- **Official documentation:** [List Assigned Conversations](https://dev.frontapp.com/reference/list-assigned-conversations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teammate_id` | path | `string` | yes | The teammate ID. |
| `q` | query | `string` | no | Search query object string for statuses or ticketing status filters. |
