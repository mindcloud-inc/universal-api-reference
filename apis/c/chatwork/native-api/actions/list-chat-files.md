# List Chat Files with Chatwork

## Endpoint

- **Method:** `GET`
- **Path:** `/rooms/:room_id/files`
- **Base URL:** `https://api.chatwork.com/v2`
- **Official documentation:** [List Chat Files](https://developer.chatwork.com/reference/get-rooms-room_id-files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Room ID. |
| `account_id` | query | `number` | no | Account ID of the file uploader. |
