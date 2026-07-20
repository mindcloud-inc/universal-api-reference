# Generate Talking Video with Easy-Peasy.AI

Generates a talking video in Easy-Peasy.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/generate-talking-video`
- **Base URL:** `https://easy-peasy.ai`
- **API:** rest
- **Official documentation:** [Generate Talking Video](https://docs.easy-peasy.ai/api-reference/endpoint/generate-talking-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `string` | no | Optional face image URL to animate. |
| `video` | body | `string` | no | Optional source video URL to lip-sync. |
| `text` | body | `string` | no | Optional speech text when you are not providing an audio file. |
| `voiceID` | body | `string` | no | Optional TTS voice identifier when using text input. |
| `audio` | body | `string` | no | Optional audio file URL to use directly. |
| `avatarModel` | body | `string` | no | Optional avatar generation mode for image-based talking videos. |
| `resolution` | body | `string` | no | Optional output resolution for the talking video. |
| `generateCaptions` | body | `boolean` | no | Whether to generate captions on the output video. |
| `captionColor` | body | `string` | no | Optional caption highlight color in hex format. |
