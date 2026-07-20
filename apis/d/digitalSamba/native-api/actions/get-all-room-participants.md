# Get all room participants with Digital Samba

Retrieves room participants from Digital Samba.

## Endpoint

- **Method:** `GET`
- **Path:** `/rooms/:room/participants`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Get all room participants](https://developer.digitalsamba.com/rest-api/#participants-GETapi-v1-rooms--room--participants)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room` | path | `string` | yes | Room path parameter. |
| `date_start` | query | `string` | no | Period start date. Must be a valid date in the format Y-m-d. |
| `date_end` | query | `string` | no | Period end date. Must be a valid date in the format Y-m-d. |
| `after` | query | `string` | no | The UUID of the room or room friendly URL after which records will be returned. |
| `live` | query | `boolean` | no | Flag to filter live or archive sessions. |
| `session_id` | query | `string` | no | The UUID of the session to filter participants by specific session. |
