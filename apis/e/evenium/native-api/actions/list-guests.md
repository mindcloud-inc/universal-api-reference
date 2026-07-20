# List Guests with Evenium

Retrieves guests from Evenium.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/guests`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [List Guests](https://static.evenium.com/api-docs/organizer/index-json.html#_get_all_guests)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `number` | yes | The Evenium event ID. |
