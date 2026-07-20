# Update a video object with api.video

Updates an existing video object in api.video.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/videos/:videoId`
- **Base URL:** `https://ws.api.video`
- **Official documentation:** [Update a video object](https://docs.api.video/reference/api/Videos#update-a-video-object)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional updated description for the video object. |
| `title` | body | `string` | no | Optional updated title for the video object. |
| `videoId` | path | `string` | yes | The unique identifier for the video. |
