# List Event Parts with Evenium

Retrieves event parts from Evenium.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/eventParts`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [List Event Parts](https://static.evenium.com/api-docs/organizer/index-json.html#_get_all_event_parts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `number` | yes | The Evenium event ID. |
