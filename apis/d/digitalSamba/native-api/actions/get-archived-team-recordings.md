# Get archived team recordings with Digital Samba

Retrieves archived team recordings from Digital Samba.

## Endpoint

- **Method:** `GET`
- **Path:** `/recordings/archived`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Get archived team recordings](https://developer.digitalsamba.com/rest-api/#recordings-GETapi-v1-recordings-archived)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | query | `string` | no | The UUID of the room. |
| `after` | query | `string` | no | The UUID of the recording after which records will be returned. |
