# Add Video to Showcase with Vimeo

Adds a video to a showcase in Vimeo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:user_id/albums/:album_id/videos/:video_id`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [Add Video to Showcase](https://developer.vimeo.com/api/reference/showcases#add_video_to_showcase)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | The ID of the user who owns the showcase. |
| `album_id` | path | `number` | yes | The ID of the showcase. |
| `video_id` | path | `number` | yes | The ID of the video to add to the showcase. |
