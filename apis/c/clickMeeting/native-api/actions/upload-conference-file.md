# Upload Conference File with ClickMeeting

Creates a conference file in ClickMeeting.

## Endpoint

- **Method:** `POST`
- **Path:** `file-library/conferences/{{room_id}}`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [Upload Conference File](https://dev.clickmeeting.com/api-doc/#post_file_library_by_conference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
| `uploaded` | body | `file` | yes | File to upload into the conference library. |
