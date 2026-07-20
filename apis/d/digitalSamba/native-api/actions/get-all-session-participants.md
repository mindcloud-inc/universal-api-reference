# Get all session participants with Digital Samba

Retrieves session participants from Digital Samba.

## Endpoint

- **Method:** `GET`
- **Path:** `/sessions/:session/participants`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Get all session participants](https://developer.digitalsamba.com/rest-api/#participants-GETapi-v1-sessions--session--participants)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session` | path | `string` | yes | Session path parameter. |
| `date_start` | query | `string` | no | Period start date. Must be a valid date in the format Y-m-d. |
| `date_end` | query | `string` | no | Period end date. Must be a valid date in the format Y-m-d. |
| `after` | query | `string` | no | The UUID of the room or room friendly URL after which records will be returned. |
| `live` | query | `boolean` | no | Flag to filter live or archive sessions. |
