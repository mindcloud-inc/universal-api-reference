# Get Room Presence with Instant

Retrieves room presence from Instant.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/rooms/presence`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Get Room Presence](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room-type` | query | `string` | yes | Room type to inspect. |
| `room-id` | query | `string` | yes | Room identifier to inspect. |
