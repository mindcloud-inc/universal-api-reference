# List Video Comments with Vimeo

Retrieves comments on a Vimeo video.

## Endpoint

- **Method:** `GET`
- **Path:** `/videos/:video_id/comments`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [List Video Comments](https://developer.vimeo.com/api/reference/videos#get_comments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_id` | path | `number` | yes | The ID of the video. |
| `direction` | query | `list` | no | The sort direction of the results. Accepted values: `asc`, `desc`. |
