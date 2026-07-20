# Update Video with Bannerbear

Updates an existing video in Bannerbear.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/videos`
- **Base URL:** `https://api.bannerbear.com`
- **Official documentation:** [Update Video](https://developers.bannerbear.com/v2/#update-a-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | body | `string` | yes | The unique ID of the video to update. |
| `transcription[]` | body | `array<string>` | no | A replacement transcription array with the same number of lines as the original. |
| `approved` | body | `boolean` | no | Approve the video and begin rendering. |
