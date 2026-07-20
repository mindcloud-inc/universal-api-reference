# Create Video with Bannerbear

Creates a new video in Bannerbear.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/videos`
- **Base URL:** `https://api.bannerbear.com`
- **Official documentation:** [Create Video](https://developers.bannerbear.com/v2/#create-a-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_template` | body | `string` | yes | The Bannerbear video template UID. |
| `input_media_url` | body | `string` | no | Input media URL for dynamic video scenes when required by the template. |
| `modifications` | body | `list<object>` | no | Layer modifications to apply when generating the video. |
| `zoom` | body | `string` | no | Zoom mode for the generated video. |
| `zoom_factor` | body | `number` | no | Zoom factor for the generated video. |
| `blur` | body | `number` | no | Blur amount for the generated video. |
| `trim_start_time` | body | `string` | no | Start time for trimming the input media. |
| `trim_end_time` | body | `string` | no | End time for trimming the input media. |
| `trim_to_length_in_seconds` | body | `number` | no | Trim the input media to a target duration in seconds. |
| `webhook_url` | body | `string` | no | Webhook URL to receive the render result. |
| `metadata` | body | `string` | no | Custom metadata to attach to the generated video. |
| `frames` | body | `list<object>` | no | Per-frame layer data for animated scenes when supported. |
| `frame_durations` | body | `list<number>` | no | Frame durations for animated video scenes. |
| `create_gif_preview` | body | `boolean` | no | Create a GIF preview for the generated video. |
