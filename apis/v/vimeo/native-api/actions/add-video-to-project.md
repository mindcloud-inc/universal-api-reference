# Add Video to Project with Vimeo

Adds a video to a project in Vimeo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:user_id/projects/:project_id/videos/:video_id`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [Add Video to Project](https://developer.vimeo.com/api/reference/folders#add_video_to_project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | The ID of the user. |
| `project_id` | path | `number` | yes | The ID of the folder. |
| `video_id` | path | `number` | yes | The ID of the video. |
