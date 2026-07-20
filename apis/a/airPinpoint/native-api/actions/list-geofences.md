# List Geofences with AirPinpoint

Retrieves configured geofences for AirPinpoint trackables.

## Endpoint

- **Method:** `GET`
- **Path:** `/geofences`
- **Base URL:** `https://api.airpinpoint.com/v1`
- **Official documentation:** [List Geofences](https://airpinpoint.com/docs/geofences)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `limit` | query | `number` | no |
| `skip` | query | `number` | no |
| `trackable_id` | query | `string` | no |
