# List Session Attendees with ClickMeeting

Retrieves attendees for a session in ClickMeeting.

## Endpoint

- **Method:** `GET`
- **Path:** `conferences/{{room_id}}/sessions/{{session_id}}/attendees`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [List Session Attendees](https://dev.clickmeeting.com/api-doc/#get_session_attendees)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
| `session_id` | path | `number` | yes | Session identifier. |
