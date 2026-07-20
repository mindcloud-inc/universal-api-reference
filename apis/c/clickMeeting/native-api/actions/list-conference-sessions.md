# List Conference Sessions with ClickMeeting

Retrieves sessions for a conference in ClickMeeting.

## Endpoint

- **Method:** `GET`
- **Path:** `conferences/{{room_id}}/sessions`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [List Conference Sessions](https://dev.clickmeeting.com/api-doc/#get_sessions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
