# Get Video with Vimeo

Retrieves a video record from Vimeo.

## Endpoint

- **Method:** `GET`
- **Path:** `/videos/:video_id`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [Get Video](https://developer.vimeo.com/api/reference/videos#get_video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_id` | path | `number` | yes | The ID of the video. |
| `time_links` | query | `boolean` | no | Whether to return timestamps in the description as links. |
