# Add Audio To Video with Bookoly

Adds audio to a video in Bookoly.

## Endpoint

- **Method:** `POST`
- **Path:** `/add-audio-to-video`
- **Base URL:** `https://bookoly.com/api/v1`
- **Official documentation:** [Add Audio To Video](https://bookoly.com/docs/api/v1#/paths/~1add-audio-to-video/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video` | body | `object` | yes |
| `video.name` | body | `string` | yes |
| `video.url` | body | `string` | yes |
| `video.mute` | body | `boolean` | yes |
| `audio` | body | `object` | yes |
| `audio.url` | body | `string` | yes |
| `audio.trim` | body | `boolean` | yes |
| `audio.volume` | body | `number` | yes |
