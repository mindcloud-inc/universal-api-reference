# Get room transcripts with Digital Samba

Retrieves room transcripts from Digital Samba.

## Endpoint

- **Method:** `GET`
- **Path:** `/rooms/:room/transcripts`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Get room transcripts](https://developer.digitalsamba.com/rest-api/#rooms-GETapi-v1-rooms--room--transcripts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room` | path | `string` | yes | Room path parameter. |
| `session_id` | query | `string` | no | UUID of the session. |
