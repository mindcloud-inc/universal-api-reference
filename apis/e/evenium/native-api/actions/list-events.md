# List Events with Evenium

Retrieves events from Evenium.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [List Events](https://static.evenium.com/api-docs/organizer/index-json.html#_get_all_events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startsAfter` | query | `date` | no | Only retrieve events which start after the given date. |
| `title` | query | `string` | no | Only retrieve events whose title is like the given title. |
