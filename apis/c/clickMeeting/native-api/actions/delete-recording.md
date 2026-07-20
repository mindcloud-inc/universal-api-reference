# Delete Recording with ClickMeeting

Deletes a recording from ClickMeeting by recording ID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `conferences/{{room_id}}/recordings/{{recording_id}}`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [Delete Recording](https://dev.clickmeeting.com/api-doc/#delete_recording)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
| `recording_id` | path | `number` | yes | Recording identifier. |
