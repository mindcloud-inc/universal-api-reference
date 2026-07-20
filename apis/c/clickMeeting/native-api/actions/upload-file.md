# Upload File with ClickMeeting

Creates a file in the ClickMeeting file library.

## Endpoint

- **Method:** `POST`
- **Path:** `file-library`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [Upload File](https://dev.clickmeeting.com/api-doc/#post_file_library)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uploaded` | body | `file` | yes | File to upload into the ClickMeeting library. |
