# Get rooms with live participants count with Digital Samba

Retrieves live participant counts for rooms in Digital Samba.

## Endpoint

- **Method:** `GET`
- **Path:** `/rooms/live`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Get rooms with live participants count](https://developer.digitalsamba.com/rest-api/#live-GETapi-v1-rooms-live)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | The UUID of the room or room friendly URL after which records will be returned. |
