# Upload Chat File with Chatwork

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms/:room_id/files`
- **Base URL:** `https://api.chatwork.com/v2`
- **Official documentation:** [Upload Chat File](https://developer.chatwork.com/reference/post-rooms-room_id-files)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Room ID. |
| `file` | body | `file` | yes | File to upload. Chatwork accepts files up to 5 MB. |
| `message` | body | `string` | no | Message text attached to the uploaded file. Maximum length: 65535. |
