# Get all team rooms with Digital Samba

Retrieves team rooms from Digital Samba.

## Endpoint

- **Method:** `GET`
- **Path:** `/rooms`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Get all team rooms](https://developer.digitalsamba.com/rest-api/#rooms-GETapi-v1-rooms)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | The UUID of the room or room friendly URL after which records will be returned. |
| `tag` | query | `string` | no | string\|array Filter rooms by tags. |
