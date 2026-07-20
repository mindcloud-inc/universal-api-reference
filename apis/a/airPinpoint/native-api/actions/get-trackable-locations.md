# Get Trackable Locations with AirPinpoint

Retrieves location data for a trackable in AirPinpoint.

## Endpoint

- **Method:** `GET`
- **Path:** `/trackables/{trackableId}/locations`
- **Base URL:** `https://api.airpinpoint.com/v1`
- **Official documentation:** [Get Trackable Locations](https://airpinpoint.com/docs/locations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | — |
| `skip` | query | `number` | no | — |
| `trackableId` | path | `string` | yes | — |
| `start_time` | query | `date` | no | Optional ISO 8601 UTC start of the history window. |
| `end_time` | query | `date` | no | Optional ISO 8601 UTC end of the history window. |
