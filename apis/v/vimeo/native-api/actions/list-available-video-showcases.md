# List Available Video Showcases with Vimeo

Retrieves showcases available for a Vimeo video.

## Endpoint

- **Method:** `GET`
- **Path:** `/videos/:video_id/available_albums`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [List Available Video Showcases](https://developer.vimeo.com/api/reference/showcases#get_available_video_showcases)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_id` | path | `number` | yes | The ID of the video. |
| `query` | query | `string` | no | Search text to filter the returned showcases. |
