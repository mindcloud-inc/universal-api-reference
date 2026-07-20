# Upload Chat File with Zoom Team Chat

## Endpoint

- **Method:** `POST`
- **Path:** `https://file.zoom.us/v2/chat/users/:userId/files`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Upload Chat File](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/uploadAChatFile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The user's ID. |
| `postToPersonalChat` | query | `boolean` | no | Whether to post the uploaded file to personal chat. |
