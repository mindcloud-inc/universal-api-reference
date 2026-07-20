# Remove Video from Project with Vimeo

Deletes a video from a project in Vimeo.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/users/:user_id/projects/:project_id/videos/:video_id`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [Remove Video from Project](https://developer.vimeo.com/api/reference/folders#remove_video_from_project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | The ID of the user. |
| `project_id` | path | `number` | yes | The ID of the folder. |
| `video_id` | path | `number` | yes | The ID of the video. |
