# Create Video From Avatar with JoggAI

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/create_video_from_avatar`
- **Base URL:** `https://api.jogg.ai`
- **Official documentation:** [Create Video From Avatar](https://docs.jogg.ai/api-reference/v2/API%20Documentation/CreateAvatarVideos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aspect_ratio` | body | `string` | yes | Video aspect ratio: portrait, landscape, or square. |
| `avatar.avatar_id` | body | `number` | yes | Avatar ID to use in the video. |
| `avatar.avatar_type` | body | `number` | yes | 0 for public avatars, 1 for custom avatars. |
| `caption` | body | `boolean` | no | Whether captions should be included in the generated video. |
| `screen_style` | body | `number` | yes | Numeric screen style variant for the output video. |
| `voice.audio_url` | body | `string` | no | Public audio URL to use when voice type is audio. |
| `voice.script` | body | `string` | yes | Script to speak when voice type is script. |
| `voice.type` | body | `string` | yes | Use script for text-to-speech or audio for an uploaded audio URL. |
| `voice.voice_id` | body | `string` | yes | Voice ID for text-to-speech generation. |
