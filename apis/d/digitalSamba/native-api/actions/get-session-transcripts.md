# Get session transcripts with Digital Samba

Retrieves session transcripts from Digital Samba.

## Endpoint

- **Method:** `GET`
- **Path:** `/sessions/:session/transcripts`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Get session transcripts](https://developer.digitalsamba.com/rest-api/#sessions-GETapi-v1-sessions--session--transcripts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session` | path | `string` | yes | Session path parameter. |
