# List Video Tags with Vimeo

Retrieves tags for a Vimeo video.

## Endpoint

- **Method:** `GET`
- **Path:** `/videos/:video_id/tags`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [List Video Tags](https://developer.vimeo.com/api/reference/videos#get_video_tags)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_id` | path | `number` | yes | The ID of the video. |
