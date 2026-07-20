# List Conference Recordings with ClickMeeting

Retrieves recordings for a conference in ClickMeeting.

## Endpoint

- **Method:** `GET`
- **Path:** `conferences/{{room_id}}/recordings`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [List Conference Recordings](https://dev.clickmeeting.com/api-doc/#get_recordings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
