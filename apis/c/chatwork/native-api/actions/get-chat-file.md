# Get Chat File with Chatwork

## Endpoint

- **Method:** `GET`
- **Path:** `/rooms/:room_id/files/:file_id`
- **Base URL:** `https://api.chatwork.com/v2`
- **Official documentation:** [Get Chat File](https://developer.chatwork.com/reference/get-rooms-room_id-files-file_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Room ID. |
| `file_id` | path | `number` | yes | File ID. |
| `create_download_url` | query | `number` | no | Set to 1 to include a temporary download URL valid for 30 seconds. |
