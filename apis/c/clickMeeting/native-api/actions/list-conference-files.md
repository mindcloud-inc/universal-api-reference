# List Conference Files with ClickMeeting

Retrieves files for a conference in ClickMeeting.

## Endpoint

- **Method:** `GET`
- **Path:** `file-library/conferences/{{room_id}}`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [List Conference Files](https://dev.clickmeeting.com/api-doc/#get_file_library_by_conference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
