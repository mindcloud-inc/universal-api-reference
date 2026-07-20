# Remove Video from Showcase with Vimeo

Deletes a video from a showcase in Vimeo.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/users/:user_id/albums/:album_id/videos/:video_id`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [Remove Video from Showcase](https://developer.vimeo.com/api/reference/showcases#remove_video_from_showcase)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | The ID of the user who owns the showcase. |
| `album_id` | path | `number` | yes | The ID of the showcase. |
| `video_id` | path | `number` | yes | The ID of the video to remove from the showcase. |
