# Delete All Conference Recordings with ClickMeeting

Deletes all conference recordings from ClickMeeting.

## Endpoint

- **Method:** `DELETE`
- **Path:** `conferences/{{room_id}}/recordings`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [Delete All Conference Recordings](https://dev.clickmeeting.com/api-doc/#delete_recordings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
