# Get all team recordings with Digital Samba

Retrieves team recordings from Digital Samba.

## Endpoint

- **Method:** `GET`
- **Path:** `/recordings`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Get all team recordings](https://developer.digitalsamba.com/rest-api/#recordings-GETapi-v1-recordings)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | query | `string` | no | The UUID of the room. |
| `session_id` | query | `string` | no | The UUID of the session. |
| `status` | query | `string` | no | Status of the recording (IN_PROGRESS, PENDING_CONVERSION, READY). |
| `after` | query | `string` | no | The UUID of the recording after which records will be returned. |
