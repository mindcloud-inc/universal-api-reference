# Get Conference Session with ClickMeeting

Retrieves a conference session from ClickMeeting.

## Endpoint

- **Method:** `GET`
- **Path:** `conferences/{{room_id}}/sessions/{{session_id}}`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [Get Conference Session](https://dev.clickmeeting.com/api-doc/#get_session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
| `session_id` | path | `number` | yes | Session identifier. |
