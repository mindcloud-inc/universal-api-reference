# List Event Part Registrations with Evenium

Retrieves event part registrations from Evenium.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/eventParts/:eventPartId/registrations`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [List Event Part Registrations](https://static.evenium.com/api-docs/organizer/index-json.html#_get_registrations_by_event_part)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `number` | yes | The Evenium eventId. |
| `eventPartId` | path | `number` | yes | The Evenium eventPartId. |
