# List Session Registrations with ClickMeeting

Retrieves registrations for a session in ClickMeeting.

## Endpoint

- **Method:** `GET`
- **Path:** `conferences/{{room_id}}/sessions/{{session_id}}/registrations`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [List Session Registrations](https://dev.clickmeeting.com/api-doc/#get_session_registrations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
| `session_id` | path | `number` | yes | Session identifier. |
